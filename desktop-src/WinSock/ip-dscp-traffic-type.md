---
description: In der folgenden Tabelle werden IP \_ DSCP \_ TRAFFIC \_ TYPE Socket-Optionen beschrieben.
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
ms.openlocfilehash: 87915dc214b0ba306b4f38dbd833b27199277564fa8c2815b9147e0d82253589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097850"
---
# <a name="ip_dscp_traffic_type"></a>\_IP-DSCP-DATENVERKEHRSTYP \_ \_

In der folgenden Tabelle werden IP \_ DSCP \_ TRAFFIC \_ TYPE Socket-Optionen beschrieben.

<dl> <dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**\_IP-DSCP-DATENVERKEHRSTYP \_ \_**</dt> <dd> <dl> <dt> 

| Option              | Herunterladen | Set | Optval-Typ | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_DSCP-DATENVERKEHRSTYP \_ | Ja | Ja | DWORD       | Durch Festlegen dieses Werts auf werte, die in **DSCP \_ TRAFFIC \_ TYPE** definiert sind, kann eine Anwendung ihre Netzwerkpakete entsprechend dem angeforderten Diensttyp behandeln. Auf ähnliche Weise können Aufrufe von [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) verwendet werden, um die aktuelle Einstellung für den Typ des für den angegebenen Socket angeforderten Datenverkehrs abzurufen. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|--------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows 10<br/>                                                          |
| Ende des Supports (Server)<br/> | Windows Server 2016<br/>                                                 |
| Header<br/>                | <dl> <dt>N/V</dt> </dl> |



 

 




