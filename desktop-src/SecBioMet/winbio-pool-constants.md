---
title: WINBIO_POOL Konstanten (winbio \_ types. h)
description: Geben Sie den Typ des biometrischen Einheiten Pools an, der in der Sitzung verwendet werden soll.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7af1ec8d5692a390bb91ecb63736bd94efb2e85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519025"
---
# <a name="winbio_pool-constants"></a>Winbio- \_ Pool Konstanten

Die folgenden Konstanten können in der [**winbioopensession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) -Funktion verwendet werden, um den Typ des biometrischen Einheiten Pools anzugeben, der in der Sitzung verwendet werden soll.



| Konstante                                                                                                                                                                                  | BESCHREIBUNG                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**winbio- \_ Pool \_ unbekannt**</dt> </dl>          | Der Pooltyp ist unbekannt.<br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**winbio- \_ Pool \_ System**</dt> </dl>             | Gibt eine freigegebene Auflistung biometrischer Einheiten an, die vom Dienstanbieter verwaltet werden.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**privater winbio- \_ Pool \_**</dt> </dl>          | Gibt eine Sammlung von biometrischen Einheiten an, die vom Aufrufer verwaltet werden.<br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <dt>**winbio- \_ Pool \_ nicht zugewiesen**</dt> </dl> | Reserviert.<br/>                                                                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Konstanten](client-application-constants.md)
</dt> </dl>

 

 





