---
description: In der folgenden Tabelle werden die \_ \_ \_ Socketoptionen für den IP-DSCP-Datenverkehr
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370099"
---
# <a name="ip_dscp_traffic_type"></a>IP- \_ DSCP- \_ \_ Datenverkehrstyp

In der folgenden Tabelle werden die \_ \_ \_ Socketoptionen für den IP-DSCP-Datenverkehr

<dl> <dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**IP- \_ DSCP- \_ \_ Datenverkehrstyp**</dt> <dd> <dl> <dt> 

| Option              | Herunterladen | Set | Optval-Typ | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DSCP- \_ Daten \_ Verkehrstyp | Ja | Ja | DWORD       | Wenn Sie diesen Wert auf Werte festlegen, die im **DSCP- \_ Daten \_ Verkehrstyp** definiert sind, kann eine Anwendung ihre Netzwerkpakete nach dem angeforderten Diensttyp Abfragen. Ähnliche Aufrufe von [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) können verwendet werden, um die aktuelle Einstellung für den Typ des für den angegebenen Socket angeforderten Datenverkehrs abzurufen. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|--------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows 10<br/>                                                          |
| Ende des Supports (Server)<br/> | Windows Server 2016<br/>                                                 |
| Header<br/>                | <dl> <dt>N/V</dt> </dl> |



 

 




