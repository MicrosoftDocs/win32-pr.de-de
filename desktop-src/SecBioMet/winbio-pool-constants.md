---
title: WINBIO_POOL Konstanten (Winbio \_ types.h)
description: Geben Sie den Typ des biometrischen Einheitenpools an, der in der Sitzung verwendet werden soll.
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
ms.openlocfilehash: fefc43bb9dc4cefbde1ce5622853a3ba2cfae498ff2f8f81e97417e306641db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909797"
---
# <a name="winbio_pool-constants"></a>WINBIO \_ POOL-Konstanten

Die folgenden Konstanten können in der [**WinBioOpenSession-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) verwendet werden, um den Typ des biometrischen Einheitenpools anzugeben, der in der Sitzung verwendet werden soll.



| Konstante                                                                                                                                                                                  | BESCHREIBUNG                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**\_WINBIO-POOL \_ UNBEKANNT**</dt> </dl>          | Der Pooltyp ist unbekannt.<br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**\_WINBIO-POOLSYSTEM \_**</dt> </dl>             | Gibt eine freigegebene Sammlung biometrischer Einheiten an, die vom Dienstanbieter verwaltet werden.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**WINBIO \_ POOL \_ PRIVATE**</dt> </dl>          | Gibt eine Auflistung biometrischer Einheiten an, die vom Aufrufer verwaltet werden.<br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <dt>**\_WINBIO-POOL \_ NICHT ZUGEWIESEN**</dt> </dl> | Reserviert.<br/>                                                                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungskonstanten](client-application-constants.md)
</dt> </dl>

 

 





