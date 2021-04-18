---
title: RPC-NDR-Schnittstellenreferenz
description: Microsoft RPC-NDR unterstützt derzeit die folgenden Funktionen und Strukturen.
ms.assetid: 2EBB2DD6-60DD-4C9F-9F79-231383B28517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a802720c584d08112c733135c3bb5640e7679c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315825"
---
# <a name="rpc-ndr-interface-reference"></a>RPC-NDR-Schnittstellenreferenz

Microsoft RPC-NDR unterstützt derzeit die folgenden Funktionen und Strukturen:

-   [**Cstdstubbuffer- \_ adressf**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_addref)
-   [**Cstdstubbuffer \_ Connect**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_connect)
-   [**Cstdstubbuffer- \_ Ratgeber**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_countrefs)
-   [**Cstdstubbuffer \_ debugserverqueryinterface**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_debugserverqueryinterface)
-   [**Cstdstubbuffer \_ debugserverrelease**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_debugserverrelease)
-   [**Cstdstubbuffer \_ trennen**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_disconnect)
-   [**Cstdstubbuffer- \_ Aufruf**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_invoke)
-   [**Cstdstubbuffer \_ isiidsupported**](/windows/desktop/api/RpcProxy/nf-rpcproxy-cstdstubbuffer_isiidsupported)
-   [**Cstdstubbuffer \_ QueryInterface**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_queryinterface)
-   [**IUnknown- \_ \_ adressproxyproxy**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_addref_proxy)
-   [**IUnknown \_ QueryInterface- \_ Proxy**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_queryinterface_proxy)
-   [**IUnknown \_ - \_ releaseproxy**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_queryinterface_proxy)
-   [**Ndrasyncclientcall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrasyncclientcall)
-   [**Ndrclearoutparameters**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclearoutparameters)
-   [**Ndrclientcallcenter**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclientcall)
-   [**NdrClientCall2**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclientcall2)
-   [**Ndrconformantarrayunmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarrayunmarshall)
-   [**Ndrconformantstringbuffersize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringbuffersize)
-   [**Ndrconformantstringmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringmarshall)
-   [**Ndrconformantstringunmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringunmarshall)
-   [**Ndrcontexthandleinitialize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandleinitialize)
-   [**Ndrcontexthandlesize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandlesize)
-   [**Ndrcontexthandlememorysize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandlememorysize)
-   [**Ndrconvert**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconvert)
-   [**Ndrcstdstubbuffer- \_ Release**](/previous-versions/aa374242(v=vs.80))
-   [**NdrCStdStubBuffer2- \_ Version**](/previous-versions/aa374240(v=vs.80))
-   [**Ndrdllcanunloadnow**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllcanunloadnow)
-   [**Ndrdllgetclassobject**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllgetclassobject)
-   [**Ndrdllregisterproxy**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllregisterproxy)
-   [**Ndrdllunregisterproxy**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllunregisterproxy)
-   [**Ndrgetusermarshalinfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
-   [**Ndrinterfacepointerbuffersize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerbuffersize)
-   [**Ndrinterfacepointerfree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerfree)
-   [**Ndrinterfacepointermarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointermarshall)
-   [**Ndrinterfacepointerunmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerunmarshall)
-   [**Ndrolezuordnen**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndroleallocate)
-   [**Ndrolefree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrolefree)
-   [**Ndrpointerbuffersize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerbuffersize)
-   [**Ndrpointerfree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerfree)
-   [**Ndrpointermarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointermarshall)
-   [**Ndrpointerunmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerunmarshall)
-   [**Ndrproxyerrorhandler**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyerrorhandler)
-   [**Ndrproxyfrebuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyfreebuffer)
-   [**Ndrproxygetbuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxygetbuffer)
-   [**Ndrproxyinitialize**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyinitialize)
-   [**Ndrproxysendreceive**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxysendreceive)
-   [**Ndrsimpletypemarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimpletypemarshall)
-   [**Ndrsimpletypeunmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimpletypeunmarshall)
-   [**NdrStubCall2**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrstubcall2)
-   [**Ndrstubforwardingfunction**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubforwardingfunction)
-   [**Ndrstubgetbuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubgetbuffer)
-   [**Ndrstubinitialize**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubinitialize)
-   [**Ndrusermarshalbuffersize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalbuffersize)
-   [**Ndrusermarshalfree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalfree)
-   [**Ndrusermarshalmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalmarshall)
-   [**mittlerer l- \_ Stub-Debug \_**](/windows/desktop/api/Rpcndr/ns-rpcndr-midl_stub_desc)
-   [**mittlere \_ Stub- \_ Nachricht**](/windows/desktop/api/Rpcndr/ns-rpcndr-midl_stub_message)
-   [**Proxyfileingefo**](/windows/win32/api/rpcproxy/ns-rpcproxy-proxyfileinfo)
-   [**RPC- \_ Nachricht**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message)

 

 