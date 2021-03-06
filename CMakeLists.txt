cmake_minimum_required(VERSION 3.12)
project(ns_2_35)

set(CMAKE_CXX_STANDARD 14)

include_directories(.)
include_directories(adc)
include_directories(aodv)
include_directories(aomdv)
include_directories(apps)
include_directories(asim)
include_directories(baytcp)
include_directories(classifier)
include_directories(common)
include_directories(dccp)
include_directories(delaybox)
include_directories(diffserv)
include_directories(diffusion)
include_directories(diffusion3/apps/gear_examples)
include_directories(diffusion3/apps/ping)
include_directories(diffusion3/apps/rmst_examples)
include_directories(diffusion3/filter_core)
include_directories(diffusion3/filters/diffusion)
include_directories(diffusion3/filters/gear)
include_directories(diffusion3/filters/misc)
include_directories(diffusion3/filters/rmst)
include_directories(diffusion3/lib)
include_directories(diffusion3/lib/main)
include_directories(diffusion3/lib/nr)
include_directories(diffusion3/ns)
include_directories(dsdv)
include_directories(dsr)
include_directories(empweb)
include_directories(emulate)
include_directories(gaf)
include_directories(imep)
include_directories(indep-utils/cmu-scen-gen/setdest)
include_directories(indep-utils/dosdbell)
include_directories(indep-utils/webtrace-conv/dec)
include_directories(indep-utils/webtrace-conv/nlanr)
include_directories(indep-utils/webtrace-conv/ucb)
include_directories(lib)
include_directories(link)
include_directories(linkstate)
include_directories(mac)
include_directories(mcast)
include_directories(mdart)
include_directories(mobile)
include_directories(mpls)
include_directories(nix)
include_directories(packmime)
include_directories(pgm)
include_directories(puma)
include_directories(pushback)
include_directories(qs)
include_directories(queue)
include_directories(rap)
include_directories(routealgo)
include_directories(routing)
include_directories(rtproto)
include_directories(satellite)
include_directories(sctp)
include_directories(sensor-nets)
include_directories(src_rtg)
include_directories(tcp)
include_directories(tcp/linux)
include_directories(tcp/linux/src)
include_directories(tmix)
include_directories(tools)
include_directories(tora)
include_directories(trace)
include_directories(webcache)
include_directories(wpan)
include_directories(xcp)

add_executable(ns_2_35
        adc/acto-adc.cc
        adc/actp-adc.cc
        adc/adaptive-receiver.cc
        adc/adaptive-receiver.h
        adc/adc.cc
        adc/adc.h
        adc/consrcvr.cc
        adc/estimator.cc
        adc/estimator.h
        adc/expavg-est.cc
        adc/hb-adc.cc
        adc/ms-adc.cc
        adc/null-estimator.cc
        adc/param-adc.cc
        adc/pointsample-est.cc
        adc/resv.cc
        adc/resv.h
        adc/sa.cc
        adc/sa.h
        adc/salink.cc
        adc/salink.h
        adc/simple-intserv-sched.cc
        adc/tbf.cc
        adc/tbf.h
        adc/timewindow-est.cc
        adc/ump.cc
        adc/ump.h
        aodv/aodv.cc
        aodv/aodv.h
        aodv/aodv_logs.cc
        aodv/aodv_packet.h
        aodv/aodv_rqueue.cc
        aodv/aodv_rqueue.h
        aodv/aodv_rtable.cc
        aodv/aodv_rtable.h
        aomdv/aomdv.cc
        aomdv/aomdv.h
        aomdv/aomdv_logs.cc
        aomdv/aomdv_packet.h
        aomdv/aomdv_rqueue.cc
        aomdv/aomdv_rqueue.h
        aomdv/aomdv_rtable.cc
        aomdv/aomdv_rtable.h
        apps/app.cc
        apps/app.h
        apps/bitops.h
        apps/pbc.cc
        apps/pbc.h
        apps/ping.cc
        apps/ping.h
        apps/rtp.cc
        apps/rtp.h
        apps/sctp_app1.cc
        apps/sctp_app1.h
        apps/telnet.cc
        apps/telnet.h
        apps/udp.cc
        apps/udp.h
        apps/vat.h
        apps/vatrcvr.cc
        apps/worm.cc
        apps/worm.h
        asim/asim.cc
        asim/asim.h
        asim/asimstd.cc
        baytcp/ftp.h
        baytcp/ftpc.cc
        baytcp/ftps.cc
        baytcp/tcp-full-bay.cc
        baytcp/tcp-full-bay.h
        classifier/classifier-addr.cc
        classifier/classifier-addr.h
        classifier/classifier-bst.cc
        classifier/classifier-hash.cc
        classifier/classifier-hash.h
        classifier/classifier-hier.cc
        classifier/classifier-hier.h
        classifier/classifier-mac.cc
        classifier/classifier-mcast.cc
        classifier/classifier-mcast.h
        classifier/classifier-mpath.cc
        classifier/classifier-port.cc
        classifier/classifier-port.h
        classifier/classifier-qs.cc
        classifier/classifier-qs.h
        classifier/classifier-virtual.cc
        classifier/classifier.cc
        classifier/classifier.h
        classifier/filter.cc
        classifier/filter.h
        common/agent.cc
        common/agent.h
        common/bi-connector.cc
        common/bi-connector.h
        common/connector.cc
        common/connector.h
        common/Decapsulator.cc
        common/Decapsulator.h
        common/encap.cc
        common/encap.h
        common/Encapsulator.cc
        common/Encapsulator.h
        common/flags.h
        common/fsm.cc
        common/fsm.h
        common/heap.h
        common/ip.cc
        common/ip.h
        common/ivs.cc
        common/location.h
        common/main-modular.cc
        common/main-monolithic.cc
        common/message.cc
        common/message.h
        common/messpass.cc
        common/messpass.h
        common/misc.cc
        common/mobilenode.cc
        common/mobilenode.h
        common/net-interface.cc
        common/net-interface.h
        common/node.cc
        common/node.h
        common/ns-process.cc
        common/ns-process.h
        common/object.cc
        common/object.h
        common/packet-stamp.h
        common/packet.cc
        common/packet.h
        common/parentnode.cc
        common/parentnode.h
        common/pkt-counter.cc
        common/ptypes2tcl.cc
        common/scheduler-map.cc
        common/scheduler.cc
        common/scheduler.h
        common/session-rtp.cc
        common/sessionhelper.cc
        common/simulator.cc
        common/simulator.h
        common/splay-scheduler.cc
        common/tclAppInit.cc
        common/timer-handler.cc
        common/timer-handler.h
        common/tkAppInit.cc
        common/tp.cc
        common/tp.h
        common/tpm.cc
        common/tpm.h
        common/ttl.cc
        common/win32.c
        dccp/bsd_queue.h
        dccp/dccp.cc
        dccp/dccp.h
        dccp/dccp_ackv.cc
        dccp/dccp_ackv.h
        dccp/dccp_opt.cc
        dccp/dccp_opt.h
        dccp/dccp_packets.cc
        dccp/dccp_packets.h
        dccp/dccp_sb.cc
        dccp/dccp_sb.h
        dccp/dccp_tcplike.cc
        dccp/dccp_tcplike.h
        dccp/dccp_tfrc.cc
        dccp/dccp_tfrc.h
        dccp/dccp_types.h
        delaybox/delaybox.cc
        delaybox/delaybox.h
        diffserv/dewp.cc
        diffserv/dewp.h
        diffserv/dsCore.cc
        diffserv/dsCore.h
        diffserv/dsEdge.cc
        diffserv/dsEdge.h
        diffserv/dsPolicy.cc
        diffserv/dsPolicy.h
        diffserv/dsred.cc
        diffserv/dsred.h
        diffserv/dsredq.cc
        diffserv/dsredq.h
        diffserv/ew.cc
        diffserv/ew.h
        diffusion/diff_header.h
        diffusion/diff_prob.cc
        diffusion/diff_prob.h
        diffusion/diff_rate.cc
        diffusion/diff_rate.h
        diffusion/diff_sink.cc
        diffusion/diff_sink.h
        diffusion/diffusion.cc
        diffusion/diffusion.h
        diffusion/flooding.cc
        diffusion/flooding.h
        diffusion/hash_table.cc
        diffusion/hash_table.h
        diffusion/iflist.cc
        diffusion/iflist.h
        diffusion/omni_mcast.cc
        diffusion/omni_mcast.h
        diffusion/routing_table.cc
        diffusion/routing_table.h
        diffusion3/apps/gear_examples/gear_common.cc
        diffusion3/apps/gear_examples/gear_common.hh
        diffusion3/apps/gear_examples/gear_receiver.cc
        diffusion3/apps/gear_examples/gear_receiver.hh
        diffusion3/apps/gear_examples/gear_sender.cc
        diffusion3/apps/gear_examples/gear_sender.hh
        diffusion3/apps/ping/1pp_ping_receiver.cc
        diffusion3/apps/ping/1pp_ping_receiver.hh
        diffusion3/apps/ping/1pp_ping_sender.cc
        diffusion3/apps/ping/1pp_ping_sender.hh
        diffusion3/apps/ping/2pp_ping_receiver.cc
        diffusion3/apps/ping/2pp_ping_receiver.hh
        diffusion3/apps/ping/2pp_ping_sender.cc
        diffusion3/apps/ping/2pp_ping_sender.hh
        diffusion3/apps/ping/ping.hh
        diffusion3/apps/ping/ping_common.cc
        diffusion3/apps/ping/push_receiver.cc
        diffusion3/apps/ping/push_receiver.hh
        diffusion3/apps/ping/push_sender.cc
        diffusion3/apps/ping/push_sender.hh
        diffusion3/apps/rmst_examples/rmst_sink.cc
        diffusion3/apps/rmst_examples/rmst_sink.hh
        diffusion3/apps/rmst_examples/rmst_source.cc
        diffusion3/apps/rmst_examples/rmst_source.hh
        diffusion3/filter_core/filter_core.cc
        diffusion3/filter_core/filter_core.hh
        diffusion3/filter_core/iolog.cc
        diffusion3/filter_core/iolog.hh
        diffusion3/filter_core/iostats.cc
        diffusion3/filter_core/iostats.hh
        diffusion3/filters/diffusion/one_phase_pull.cc
        diffusion3/filters/diffusion/one_phase_pull.hh
        diffusion3/filters/diffusion/two_phase_pull.cc
        diffusion3/filters/diffusion/two_phase_pull.hh
        diffusion3/filters/gear/gear.cc
        diffusion3/filters/gear/gear.hh
        diffusion3/filters/gear/gear_attr.cc
        diffusion3/filters/gear/gear_attr.hh
        diffusion3/filters/gear/gear_tools.cc
        diffusion3/filters/gear/gear_tools.hh
        diffusion3/filters/misc/log.cc
        diffusion3/filters/misc/log.hh
        diffusion3/filters/misc/srcrt.cc
        diffusion3/filters/misc/srcrt.hh
        diffusion3/filters/misc/tag.cc
        diffusion3/filters/misc/tag.hh
        diffusion3/filters/rmst/rmst.cc
        diffusion3/filters/rmst/rmst.hh
        diffusion3/filters/rmst/rmst_filter.cc
        diffusion3/filters/rmst/rmst_filter.hh
        diffusion3/lib/main/attrs.cc
        diffusion3/lib/main/attrs.hh
        diffusion3/lib/main/config.hh
        diffusion3/lib/main/events.cc
        diffusion3/lib/main/events.hh
        diffusion3/lib/main/filter.hh
        diffusion3/lib/main/header.hh
        diffusion3/lib/main/iodev.cc
        diffusion3/lib/main/iodev.hh
        diffusion3/lib/main/iohook.cc
        diffusion3/lib/main/iohook.hh
        diffusion3/lib/main/message.cc
        diffusion3/lib/main/message.hh
        diffusion3/lib/main/timers.cc
        diffusion3/lib/main/timers.hh
        diffusion3/lib/main/tools.cc
        diffusion3/lib/main/tools.hh
        diffusion3/lib/nr/nr.cc
        diffusion3/lib/nr/nr.hh
        diffusion3/lib/diffapp.cc
        diffusion3/lib/diffapp.hh
        diffusion3/lib/dr.cc
        diffusion3/lib/dr.hh
        diffusion3/ns/diffagent.cc
        diffusion3/ns/diffagent.h
        diffusion3/ns/diffrtg.cc
        diffusion3/ns/diffrtg.h
        diffusion3/ns/difftimer.cc
        diffusion3/ns/difftimer.h
        dsdv/dsdv.cc
        dsdv/dsdv.h
        dsdv/rtable.cc
        dsdv/rtable.h
        dsr/add_sr.cc
        dsr/cache_stats.h
        dsr/constants.h
        dsr/dsr_proto.cc
        dsr/dsr_proto.h
        dsr/dsragent.cc
        dsr/dsragent.h
        dsr/flowstruct.cc
        dsr/flowstruct.h
        dsr/hdr_sr.cc
        dsr/hdr_sr.h
        dsr/linkcache.cc
        dsr/mobicache.cc
        dsr/path.cc
        dsr/path.h
        dsr/requesttable.cc
        dsr/requesttable.h
        dsr/routecache.cc
        dsr/routecache.h
        dsr/simplecache.cc
        dsr/sr_forwarder.cc
        dsr/sr_forwarder.h
        dsr/srpacket.h
        empweb/empftp.cc
        empweb/empftp.h
        empweb/empweb.cc
        empweb/empweb.h
        empweb/persconn.h
        emulate/arp.cc
        emulate/ether.cc
        emulate/ether.h
        emulate/icmp.cc
        emulate/inet.c
        emulate/inet.h
        emulate/internet.cc
        emulate/internet.h
        emulate/iptap.cc
        emulate/iptap.h
        emulate/nat.cc
        emulate/net-ip.cc
        emulate/net-pcap.cc
        emulate/net.cc
        emulate/net.h
        emulate/ping_responder.cc
        emulate/tap.cc
        emulate/tap.h
        emulate/tcptap.cc
        emulate/tcptap.h
        gaf/gaf.cc
        gaf/gaf.h
        gen/ns_tcl.cc
        gen/ptypes.cc
        gen/version.c
        imep/dest_queue.cc
        imep/dest_queue.h
        imep/imep.cc
        imep/imep.h
        imep/imep_api.cc
        imep/imep_io.cc
        imep/imep_rt.cc
        imep/imep_spec.h
        imep/imep_stats.h
        imep/imep_timers.cc
        imep/imep_util.cc
        imep/rxmit_queue.cc
        imep/rxmit_queue.h
        indep-utils/cmu-scen-gen/setdest/calcdest.cc
        indep-utils/cmu-scen-gen/setdest/setdest.cc
        indep-utils/cmu-scen-gen/setdest/setdest.h
        indep-utils/cmu-scen-gen/setdest/setdest2.cc
        indep-utils/dosdbell/dosdbell.c
        indep-utils/dosdbell/dosdbell.h
        indep-utils/dosdbell/dosdbellasim.c
        indep-utils/dosdbell/dostraffic.c
        indep-utils/dosdbell/dostraffic.h
        indep-utils/dosdbell/flowlist.c
        indep-utils/dosdbell/flowlist.h
        indep-utils/dosdbell/models.c
        indep-utils/dosdbell/models.h
        indep-utils/dosreduce/dosreduce.c
        indep-utils/model-gen/http_active.c
        indep-utils/model-gen/http_connect.c
        indep-utils/propagation/threshold.cc
        indep-utils/webtrace-conv/dec/formsquid.cc
        indep-utils/webtrace-conv/dec/formtxt.cc
        indep-utils/webtrace-conv/dec/my-endian.cc
        indep-utils/webtrace-conv/dec/my-endian.h
        indep-utils/webtrace-conv/dec/proxytrace.cc
        indep-utils/webtrace-conv/dec/proxytrace.h
        indep-utils/webtrace-conv/dec/proxytrace2any.cc
        indep-utils/webtrace-conv/dec/tr-stat.cc
        indep-utils/webtrace-conv/epa/tr-stat.cc
        indep-utils/webtrace-conv/nlanr/logparse.cc
        indep-utils/webtrace-conv/nlanr/logparse.h
        indep-utils/webtrace-conv/nlanr/tr-stat.cc
        indep-utils/webtrace-conv/ucb/config.h
        indep-utils/webtrace-conv/ucb/logparse.cc
        indep-utils/webtrace-conv/ucb/logparse.h
        indep-utils/webtrace-conv/ucb/tr-stat.cc
        indep-utils/webtrace-conv/ucb/utils.cc
        indep-utils/webtrace-conv/ucb/utils.h
        lib/bsd-list.h
        lib/builtin.h
        lib/dmalloc_support.cc
        lib/int.defs.h
        lib/int.RVec.cc
        lib/int.RVec.h
        lib/int.Vec.cc
        lib/int.Vec.h
        link/delay.cc
        link/delay.h
        link/dynalink.cc
        link/hackloss.cc
        linkstate/hdr-ls.cc
        linkstate/hdr-ls.h
        linkstate/ls.cc
        linkstate/ls.h
        linkstate/rtProtoLS.cc
        linkstate/rtProtoLS.h
        mac/arp.cc
        mac/arp.h
        mac/channel.cc
        mac/channel.h
        mac/lanRouter.cc
        mac/lanRouter.h
        mac/ll.cc
        mac/ll.h
        mac/mac-802_11.cc
        mac/mac-802_11.h
        mac/mac-802_11Ext.cc
        mac/mac-802_11Ext.h
        mac/mac-802_3.cc
        mac/mac-802_3.h
        mac/mac-csma.cc
        mac/mac-csma.h
        mac/mac-multihop.cc
        mac/mac-multihop.h
        mac/mac-simple.cc
        mac/mac-simple.h
        mac/mac-tdma.cc
        mac/mac-tdma.h
        mac/mac-timers.cc
        mac/mac-timers.h
        mac/mac.cc
        mac/mac.h
        mac/marshall.h
        mac/phy.cc
        mac/phy.h
        mac/smac.cc
        mac/smac.h
        mac/varp.cc
        mac/varp.h
        mac/wired-phy.cc
        mac/wired-phy.h
        mac/wireless-phy.cc
        mac/wireless-phy.h
        mac/wireless-phyExt.cc
        mac/wireless-phyExt.h
        mcast/classifier-lms.cc
        mcast/ctrMcast.cc
        mcast/ctrMcast.h
        mcast/lms-agent.cc
        mcast/lms-receiver.cc
        mcast/lms-sender.cc
        mcast/lms.h
        mcast/mcast_ctrl.cc
        mcast/mcast_ctrl.h
        mcast/rcvbuf.cc
        mcast/rcvbuf.h
        mcast/replicator.cc
        mcast/rlm.cc
        mcast/srm-headers.h
        mcast/srm-ssm.cc
        mcast/srm-ssm.h
        mcast/srm-state.h
        mcast/srm-topo.cc
        mcast/srm-topo.h
        mcast/srm.cc
        mcast/srm.h
        mdart/mdart.cc
        mdart/mdart.h
        mdart/mdart_adp.cc
        mdart/mdart_adp.h
        mdart/mdart_dht.cc
        mdart/mdart_dht.h
        mdart/mdart_function.h
        mdart/mdart_ndp.cc
        mdart/mdart_ndp.h
        mdart/mdart_neighbor.cc
        mdart/mdart_neighbor.h
        mdart/mdart_packet.h
        mdart/mdart_queue.cc
        mdart/mdart_queue.h
        mdart/mdart_table.cc
        mdart/mdart_table.h
        mobile/antenna.cc
        mobile/antenna.h
        mobile/dem.cc
        mobile/dem.h
        mobile/dumb-agent.cc
        mobile/dumb-agent.h
        mobile/energy-model.cc
        mobile/energy-model.h
        mobile/god.cc
        mobile/god.h
        mobile/gridkeeper.cc
        mobile/gridkeeper.h
        mobile/mip-reg.cc
        mobile/mip.cc
        mobile/mip.h
        mobile/modulation.cc
        mobile/modulation.h
        mobile/nakagami.cc
        mobile/nakagami.h
        mobile/omni-antenna.cc
        mobile/omni-antenna.h
        mobile/propagation.cc
        mobile/propagation.h
        mobile/shadowing-vis.cc
        mobile/shadowing-vis.h
        mobile/shadowing.cc
        mobile/shadowing.h
        mobile/topography.cc
        mobile/topography.h
        mobile/tworayground.cc
        mobile/tworayground.h
        mpls/classifier-addr-mpls.cc
        mpls/classifier-addr-mpls.h
        mpls/ldp.cc
        mpls/ldp.h
        mpls/mpls-module.cc
        mpls/mpls-module.h
        nix/classifier-nix.cc
        nix/classifier-nix.h
        nix/hdr_nv.cc
        nix/hdr_nv.h
        nix/nixnode.cc
        nix/nixnode.h
        nix/nixroute.cc
        nix/nixvec.cc
        nix/nixvec.h
        packmime/packmime_HTTP.cc
        packmime/packmime_HTTP.h
        packmime/packmime_HTTP_rng.cc
        packmime/packmime_OL.cc
        packmime/packmime_OL.h
        packmime/packmime_OL_ranvar.cc
        packmime/packmime_OL_ranvar.h
        packmime/packmime_ranvar.cc
        packmime/packmime_ranvar.h
        pgm/classifier-pgm.cc
        pgm/pgm-agent.cc
        pgm/pgm-receiver.cc
        pgm/pgm-sender.cc
        pgm/pgm.h
        plm/cbr-traffic-PP.cc
        plm/loss-monitor-plm.cc
        puma/puma.cc
        puma/puma.h
        puma/puma_pkt.h
        pushback/agg-spec.cc
        pushback/agg-spec.h
        pushback/ident-tree.cc
        pushback/ident-tree.h
        pushback/logging-data-struct.cc
        pushback/logging-data-struct.h
        pushback/pushback-constants.h
        pushback/pushback-message.h
        pushback/pushback-queue.cc
        pushback/pushback-queue.h
        pushback/pushback.cc
        pushback/pushback.h
        pushback/rate-estimator.cc
        pushback/rate-estimator.h
        pushback/rate-limit-strategy.cc
        pushback/rate-limit-strategy.h
        pushback/rate-limit.cc
        pushback/rate-limit.h
        qs/hdr_qs.cc
        qs/hdr_qs.h
        qs/qsagent.cc
        qs/qsagent.h
        queue/cbq.cc
        queue/delayer.cc
        queue/delayer.h
        queue/delaymodel.cc
        queue/delaymodel.h
        queue/demarker.cc
        queue/demarker.h
        queue/drop-tail.cc
        queue/drop-tail.h
        queue/drr.cc
        queue/dsr-priqueue.cc
        queue/dsr-priqueue.h
        queue/errmodel.cc
        queue/errmodel.h
        queue/fec.cc
        queue/fec.h
        queue/fq.cc
        queue/gk.cc
        queue/gk.h
        queue/jobs.cc
        queue/jobs.h
        queue/marker.cc
        queue/marker.h
        queue/pi.cc
        queue/pi.h
        queue/priqueue.cc
        queue/priqueue.h
        queue/queue.cc
        queue/queue.h
        queue/red-pd.cc
        queue/red-pd.h
        queue/red.cc
        queue/red.h
        queue/rem.cc
        queue/rem.h
        queue/rio.cc
        queue/rio.h
        queue/rtqueue.cc
        queue/rtqueue.h
        queue/semantic-packetqueue.cc
        queue/semantic-packetqueue.h
        queue/semantic-red.cc
        queue/semantic-rio.cc
        queue/sfq.cc
        queue/srr.cc
        queue/vq.cc
        queue/vq.h
        queue/wss.h
        rap/media-app.cc
        rap/media-app.h
        rap/rap.cc
        rap/rap.h
        rap/raplist.cc
        rap/raplist.h
        rap/utilities.cc
        rap/utilities.h
        realaudio/realaudio.cc
        routealgo/bfs.cc
        routealgo/bfs.h
        routealgo/dijkstra.cc
        routealgo/dijkstra.h
        routealgo/rbitmap.cc
        routealgo/rbitmap.h
        routealgo/rlookup.cc
        routealgo/rlookup.h
        routealgo/rnode.cc
        routealgo/rnode.h
        routealgo/routealgo.cc
        routealgo/routealgo.h
        routealgo/tnode.cc
        routealgo/tnode.h
        routing/addr-params.cc
        routing/addr-params.h
        routing/address.cc
        routing/address.h
        routing/alloc-address.cc
        routing/route.cc
        routing/route.h
        routing/rtmodule.cc
        routing/rtmodule.h
        routing/rtProtoDV.cc
        routing/rtProtoDV.h
        routing/rttable.cc
        routing/rttable.h
        rtproto/rtproto.h
        satellite/sat-hdlc.cc
        satellite/sat-hdlc.h
        satellite/satgeometry.cc
        satellite/satgeometry.h
        satellite/sathandoff.cc
        satellite/sathandoff.h
        satellite/satlink.cc
        satellite/satlink.h
        satellite/satnode.cc
        satellite/satnode.h
        satellite/satposition.cc
        satellite/satposition.h
        satellite/satroute.cc
        satellite/satroute.h
        satellite/sattrace.cc
        satellite/sattrace.h
        sctp/sctp-cmt.cc
        sctp/sctp-cmt.h
        sctp/sctp-hbAfterRto.cc
        sctp/sctp-hbAfterRto.h
        sctp/sctp-mfrHbAfterRto.cc
        sctp/sctp-mfrHbAfterRto.h
        sctp/sctp-mfrTimestamp.cc
        sctp/sctp-mfrTimestamp.h
        sctp/sctp-multipleFastRtx.cc
        sctp/sctp-multipleFastRtx.h
        sctp/sctp-newreno.cc
        sctp/sctp-newreno.h
        sctp/sctp-timestamp.cc
        sctp/sctp-timestamp.h
        sctp/sctp.cc
        sctp/sctp.h
        sctp/sctpDebug.cc
        sctp/sctpDebug.h
        sensor-nets/agent-list.cc
        sensor-nets/agent-list.h
        sensor-nets/flood-agent.cc
        sensor-nets/flood-agent.h
        sensor-nets/landmark.cc
        sensor-nets/landmark.h
        sensor-nets/sensor-query.cc
        sensor-nets/sensor-query.h
        sensor-nets/tags.cc
        sensor-nets/tags.h
        src_rtg/classifier-sr.cc
        src_rtg/classifier-sr.h
        src_rtg/hdr_src.cc
        src_rtg/hdr_src.h
        src_rtg/sragent.cc
        src_rtg/sragent.h
        tcl/ex/picoeff.m
        tcp/linux/src/tcp_bic.c
        tcp/linux/src/tcp_compound.c
        tcp/linux/src/tcp_cong.c
        tcp/linux/src/tcp_cubic.c
        tcp/linux/src/tcp_highspeed.c
        tcp/linux/src/tcp_htcp.c
        tcp/linux/src/tcp_hybla.c
        tcp/linux/src/tcp_illinois.c
        tcp/linux/src/tcp_lp.c
        tcp/linux/src/tcp_scalable.c
        tcp/linux/src/tcp_vegas.c
        tcp/linux/src/tcp_vegas.h
        tcp/linux/src/tcp_veno.c
        tcp/linux/src/tcp_westwood.c
        tcp/linux/src/tcp_yeah.c
        tcp/linux/ns-linux-c.c
        tcp/linux/ns-linux-c.h
        tcp/linux/ns-linux-param.c
        tcp/linux/ns-linux-param.h
        tcp/linux/ns-linux-util.cc
        tcp/linux/ns-linux-util.h
        tcp/linux/tcp_naivereno.c
        tcp/ack-recons.cc
        tcp/ack-recons.h
        tcp/chost.cc
        tcp/chost.h
        tcp/formula-with-inverse.h
        tcp/formula.h
        tcp/nilist.cc
        tcp/nilist.h
        tcp/rq.cc
        tcp/rq.h
        tcp/rtcp.cc
        tcp/saack.cc
        tcp/scoreboard-rh.cc
        tcp/scoreboard-rh.h
        tcp/scoreboard-rq.cc
        tcp/scoreboard-rq.h
        tcp/scoreboard.cc
        tcp/scoreboard.h
        tcp/scoreboard1.cc
        tcp/scoreboard1.h
        tcp/snoop.cc
        tcp/snoop.h
        tcp/tcp-abs.cc
        tcp/tcp-abs.h
        tcp/tcp-asym-fs.cc
        tcp/tcp-asym-sink.cc
        tcp/tcp-asym.cc
        tcp/tcp-asym.h
        tcp/tcp-fack.cc
        tcp/tcp-fack.h
        tcp/tcp-fs.cc
        tcp/tcp-fs.h
        tcp/tcp-full.cc
        tcp/tcp-full.h
        tcp/tcp-int.cc
        tcp/tcp-int.h
        tcp/tcp-linux.cc
        tcp/tcp-linux.h
        tcp/tcp-newreno.cc
        tcp/tcp-rbp.cc
        tcp/tcp-reno.cc
        tcp/tcp-rfc793edu.cc
        tcp/tcp-rfc793edu.h
        tcp/tcp-sack-rh.cc
        tcp/tcp-sack1.cc
        tcp/tcp-session.cc
        tcp/tcp-session.h
        tcp/tcp-sink.cc
        tcp/tcp-sink.h
        tcp/tcp-vegas.cc
        tcp/tcp.cc
        tcp/tcp.h
        tcp/tcplib-telnet.cc
        tcp/template.h
        tcp/tfrc-sink.cc
        tcp/tfrc-sink.h
        tcp/tfrc.cc
        tcp/tfrc.h
        tmix/tmix.cc
        tmix/tmix.h
        tmix/tmix_delaybox.cc
        tmix/tmix_delaybox.h
        tmix/tmixAgent.cc
        tmix/tmixAgent.h
        tools/cbr_traffic.cc
        tools/expoo.cc
        tools/flowmon.cc
        tools/flowmon.h
        tools/integrator.cc
        tools/integrator.h
        tools/loss-monitor.cc
        tools/loss-monitor.h
        tools/measuremod.cc
        tools/measuremod.h
        tools/mem-trace.h
        tools/pareto.cc
        tools/queue-monitor.cc
        tools/queue-monitor.h
        tools/random.cc
        tools/random.h
        tools/ranvar.cc
        tools/ranvar.h
        tools/rng.cc
        tools/rng.h
        tools/trafgen.cc
        tools/trafgen.h
        tora/tora.cc
        tora/tora.h
        tora/tora_api.cc
        tora/tora_dest.cc
        tora/tora_dest.h
        tora/tora_io.cc
        tora/tora_logs.cc
        tora/tora_neighbor.cc
        tora/tora_neighbor.h
        tora/tora_packet.h
        trace/basetrace.cc
        trace/basetrace.h
        trace/cmu-trace.cc
        trace/cmu-trace.h
        trace/trace-ip.cc
        trace/trace.cc
        trace/trace.h
        trace/traffictrace.cc
        webcache/http-aux.cc
        webcache/http-aux.h
        webcache/http.cc
        webcache/http.h
        webcache/inval-agent.cc
        webcache/inval-agent.h
        webcache/logweb.cc
        webcache/logweb.h
        webcache/mcache.cc
        webcache/mcache.h
        webcache/pagepool.cc
        webcache/pagepool.h
        webcache/tcp-simple.cc
        webcache/tcp-simple.h
        webcache/tcpapp.cc
        webcache/tcpapp.h
        webcache/webserver.cc
        webcache/webserver.h
        webcache/webtraf.cc
        webcache/webtraf.h
        wpan/p802_15_4const.h
        wpan/p802_15_4csmaca.cc
        wpan/p802_15_4csmaca.h
        wpan/p802_15_4def.h
        wpan/p802_15_4fail.cc
        wpan/p802_15_4fail.h
        wpan/p802_15_4field.h
        wpan/p802_15_4hlist.cc
        wpan/p802_15_4hlist.h
        wpan/p802_15_4mac.cc
        wpan/p802_15_4mac.h
        wpan/p802_15_4nam.cc
        wpan/p802_15_4nam.h
        wpan/p802_15_4phy.cc
        wpan/p802_15_4phy.h
        wpan/p802_15_4pkt.h
        wpan/p802_15_4sscs.cc
        wpan/p802_15_4sscs.h
        wpan/p802_15_4timer.cc
        wpan/p802_15_4timer.h
        wpan/p802_15_4trace.cc
        wpan/p802_15_4trace.h
        wpan/p802_15_4transac.cc
        wpan/p802_15_4transac.h
        xcp/xcp-end-sys.cc
        xcp/xcp-end-sys.h
        xcp/xcp.cc
        xcp/xcp.h
        xcp/xcpq.cc
        xcp/xcpq.h
        autoconf-win32.h
        autoconf.h
        config.h
        ns_tclsh.cc)
