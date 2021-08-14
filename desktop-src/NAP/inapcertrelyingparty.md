---
title: INapCertRelyingParty-Schnittstelle (NapCertRelyingParty.h)
description: Zertifikatvertrauliche Parteien müssen verwenden, um mit napAgent zu kommunizieren.
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- INapCertRelyingParty-Schnittstelle NAP
- INapCertRelyingParty-Schnittstelle NAP , beschrieben
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
ms.openlocfilehash: 6d2a68c6ce910fa63588df1fa7bc1834f6ed537a2a2c9b85f24d383497a8d463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368609"
---
# <a name="inapcertrelyingparty-interface"></a>INapCertRelyingParty-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapCertRelyingParty-Schnittstelle** stellt Methoden bereit, die von zertifikatvertrauenden Seiten für die Kommunikation mit NapAgent verwendet werden müssen.

## <a name="members"></a>Member

Die **INapCertRelyingParty-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapCertRelyingParty** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapCertRelyingParty-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                        | BESCHREIBUNG                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**INapCertRelyingParty::GetSubscribedRelyingLöschs**](inapcertrelyingparty-getsubscribedrelyingparties.md) | Ruft eine Liste der vertrauenden Seiten ab, die abonniert haben.<br/>                 |
| [**INapCertRelyingParty::SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md)               | Abonniert einen bereits registrierten Integritätszertifikatserver (HCS).<br/> |
| [**INapCertRelyingParty::UnSubscribeCertByGroup**](inapcertrelyingparty-unsubscribecertbygroup.md)           | Kündigen des Abonnements von einem HCS-Server.<br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapCertRelyingParty.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCertRelyingParty.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

