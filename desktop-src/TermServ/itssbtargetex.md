---
title: Itssbtargetex-Schnittstelle
description: Macht Eigenschaften verfügbar, die Konfigurations-und Zustandsinformationen zu einem Ziel speichern.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- Itssbtargetex-Schnittstelle Remotedesktopdienste
- Itssbtargetex-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d53d126d9419f87d91b027b0d69847f67de84be6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957129"
---
# <a name="itssbtargetex-interface"></a>Itssbtargetex-Schnittstelle

Macht Eigenschaften verfügbar, die Konfigurations-und Zustandsinformationen zu einem Ziel speichern.

Diese Schnittstelle ist nur unter Windows Server 2012 R2 mit installiertem [KB3091411](https://support.microsoft.com/kb/3091411) verfügbar. Die [**targetload**](itssbtarget-targetload.md) -Eigenschaft der [**itssbtarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) -Schnittstelle ist ab Windows Server 2016 verfügbar.

## <a name="members"></a>Member

Die **itssbtargetex** -Schnittstelle erbt von [**itssbtarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget). **Itssbtargetex** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **itssbtargetex** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                      | Zugriffstyp           | BESCHREIBUNG                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**EnvironmentName**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | Lesen/Schreiben<br/> | Ruft den Namen der Umgebung ab, die dem Ziel zugeordnet ist, oder legt ihn fest.<br/> |
| [**Farmname**](itssbtarget-farmname.md)<br/>                           | Lesen/Schreiben<br/> | Gibt den Namen der Farm an, mit der dieses Ziel verknüpft ist, oder ruft ihn ab.<br/>    |
| [**IpAddresses**](itssbtarget-ipaddresses.md)<br/>                     | Lesen/Schreiben<br/> | Ruft die externen IP-Adressen des Ziels ab oder legt Sie fest.<br/>                |
| [**Numpenidingconnections**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | Schreibgeschützt<br/>  | Ruft die Anzahl der ausstehenden Benutzer Verbindungen für das Ziel ab.<br/>               |
| [**Numsessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | Schreibgeschützt<br/>  | Ruft die Anzahl der Sitzungen ab, die vom Broker für das Ziel verwaltet werden.<br/>          |
| [**Target-qdn**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | Lesen/Schreiben<br/> | Gibt den voll qualifizierten Domänen Namen des Ziels an oder ruft ihn ab.<br/>          |
| [**Targetload**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))<br/>                     | Schreibgeschützt<br/>  | Ruft die relative Auslastung eines Ziels ab.<br/>                                       |
| [**TargetName**](itssbtarget-targetname.md)<br/>                       | Lesen/Schreiben<br/> | Gibt den Namen des Ziels an oder ruft ihn ab.<br/>                                 |
| [**Targetnetbios**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | Lesen/Schreiben<br/> | Gibt den NetBIOS-Namen des Ziels an oder ruft ihn ab.<br/>                         |
| [**Targetpropertyset**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | Lesen/Schreiben<br/> | Gibt die für das Ziel festgelegte Eigenschaft an oder ruft diese ab.<br/>                        |
| [**TargetState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | Lesen/Schreiben<br/> | Gibt den Ziel Status an oder ruft ihn ab.<br/>                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                |
| IID<br/>                      | IID \_ itssbtargetex ist als 74f 99987-625d-11e5-bea1-a0481c7e9064 definiert<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbtarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[Remotedesktop Virtualisierungsschnittstellen](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

