---
title: Inapcertrelyingparty-Schnittstelle (napcertrelyingparty. h)
description: Zertifikat abhängige Seiten müssen für die Kommunikation mit dem NAPAgent verwenden.
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- Inapcertrelyingparty-Schnittstelle NAP
- Inapcertrelyingparty-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapCertRelyingParty
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b4439389c6ee65076f710bb6ea752c73a51ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040779"
---
# <a name="inapcertrelyingparty-interface"></a>Inapcertrelyingparty-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapcertrelyingparty** -Schnittstelle stellt Methoden bereit, die von Zertifikat vertrauenden Seiten für die Kommunikation mit dem NAPAgent verwendet werden müssen.

## <a name="members"></a>Member

Die **inapcertrelyingparty** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapcertrelyingparty** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapcertrelyingparty** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                        | BESCHREIBUNG                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**Inapcertrelyingparty:: getabonbedrelyingparties**](inapcertrelyingparty-getsubscribedrelyingparties.md) | Ruft eine Liste der vertrauenden Seiten ab, die abonniert haben.<br/>                 |
| [**Inapcertrelyingparty:: abonnebecertbygroup**](inapcertrelyingparty-subscribecertbygroup.md)               | Abonniert einen bereits registrierten Integritäts Zertifikat Server (HCS).<br/> |
| [**Inapcertrelyingparty:: unabonnebecertbygroup**](inapcertrelyingparty-unsubscribecertbygroup.md)           | Kündigen von einem HCS-Server.<br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>Napcertrelyingparty. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcertrelyingparty. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

