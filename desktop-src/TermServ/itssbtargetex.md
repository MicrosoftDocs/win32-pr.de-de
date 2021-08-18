---
title: ITsSbTargetEx-Schnittstelle
description: Macht Eigenschaften verfügbar, die Konfigurations- und Statusinformationen zu einem Ziel speichern.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- ITsSbTargetEx-Schnittstelle Remotedesktopdienste
- ITsSbTargetEx-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fb9be0e4cf5c0395efa93d308fdfa45362a7ac8919ab49a108700106aff6081b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989820"
---
# <a name="itssbtargetex-interface"></a>ITsSbTargetEx-Schnittstelle

Macht Eigenschaften verfügbar, die Konfigurations- und Statusinformationen zu einem Ziel speichern.

Diese Schnittstelle ist nur auf Windows Server 2012 R2 mit installierter [KB3091411](https://support.microsoft.com/kb/3091411) verfügbar. Die [**TargetLoad-Eigenschaft**](itssbtarget-targetload.md) der [**ITsSbTarget-Schnittstelle**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) ist ab Windows Server 2016 verfügbar.

## <a name="members"></a>Member

Die **ITsSbTargetEx-Schnittstelle** erbt von [**ITsSbTarget.**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) **ITsSbTargetEx** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ITsSbTargetEx-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                      | Zugriffstyp           | Beschreibung                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**EnvironmentName**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | Lesen/Schreiben<br/> | Ruft den Namen der Umgebung ab, die dem Ziel zugeordnet ist, oder gibt den Namen an.<br/> |
| [**FarmName**](itssbtarget-farmname.md)<br/>                           | Lesen/Schreiben<br/> | Gibt den Namen der Farm an, mit der dieses Ziel verknüpft ist, oder ruft diesen ab.<br/>    |
| [**Ipaddresses**](itssbtarget-ipaddresses.md)<br/>                     | Lesen/Schreiben<br/> | Ruft die externen IP-Adressen des Ziels ab oder gibt sie an.<br/>                |
| [**NumPendingConnections**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | Schreibgeschützt<br/>  | Ruft die Anzahl der ausstehenden Benutzerverbindungen für das Ziel ab.<br/>               |
| [**NumSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | Schreibgeschützt<br/>  | Ruft die Anzahl der Sitzungen ab, die vom Broker für das Ziel verwaltet werden.<br/>          |
| [**TargetFQDN**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | Lesen/Schreiben<br/> | Gibt den vollqualifizierten Domänennamen des Ziels an oder ruft sie ab.<br/>          |
| [**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))<br/>                     | Schreibgeschützt<br/>  | Ruft die relative Last auf einem Ziel ab.<br/>                                       |
| [**Targetname**](itssbtarget-targetname.md)<br/>                       | Lesen/Schreiben<br/> | Gibt den Namen des Ziels an oder ruft den Namen ab.<br/>                                 |
| [**TargetNetbios**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | Lesen/Schreiben<br/> | Gibt den NetBIOS-Namen des Ziels an oder ruft sie ab.<br/>                         |
| [**TargetPropertySet**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | Lesen/Schreiben<br/> | Gibt den Eigenschaftensatz für das Ziel an oder ruft sie ab.<br/>                        |
| [**TargetState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | Lesen/Schreiben<br/> | Gibt den Zielzustand an oder ruft den Zielzustand ab.<br/>                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                |
| IID<br/>                      | IID \_ ITsSbTargetEx ist als 74f99987-625d-11e5-bea1-a0481c7e9064 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[Remotedesktop-Virtualisierungsschnittstellen](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

