---
description: Die scesvasetachmentupdate-Funktion wird von den Snap-Ins für die Sicherheitskonfiguration aufgerufen, um Konfigurationsänderungen an die Sicherheitsdatenbank zu übergeben.
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: Scesvcalltachmentupdate-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5bc4c9426f6a085c72f2fc3d872de4d7da59156b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750865"
---
# <a name="scesvcattachmentupdate-callback-function"></a>Scesvcalltachmentupdate-Rückruffunktion

Die **scesvasetachmentupdate** -Funktion wird von den Snap-Ins für die Sicherheitskonfiguration aufgerufen, um Konfigurationsänderungen an die Sicherheitsdatenbank zu übergeben.

## <a name="syntax"></a>Syntax


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pscecbinfo* \[ in\]
</dt> <dd>

Zeiger auf eine [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur, die das Rückruf Handle und Funktionszeiger auf SCE enthält.

</dd> <dt>

*Serviceingefo* \[ in\]
</dt> <dd>

Aktualisierte Konfigurationsinformationen. Die Datenstruktur, die für diese Informationen verwendet wird, sind [**scesvc- \_ Konfigurations \_ Informationen**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird "scestatus Success" zurückgegeben \_ . Andernfalls wird ein Fehlercode zurückgegeben. Weitere Informationen zu den Sicherheits Konfigurations-Fehlercodes finden Sie unter [Anhang Return Values](management-return-values.md).

## <a name="remarks"></a>Bemerkungen

Die **scesvtortachmentupdate** -Funktion muss folgende Aktionen ausführen:

-   Rufen Sie die Rückruffunktion auf, auf die vom **pfqueryinfo** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfqueryinfo) verwiesen wird, um die aktuellen Basis Konfigurationsinformationen aus der Sicherheitsdatenbank abzurufen.
-   Rufen Sie die Rückruffunktion auf, auf die vom **pfqueryinfo** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfqueryinfo) verwiesen wird, um den letzten Satz von unterschieden (Analyse Informationen) aus der Sicherheitsdatenbank abzurufen.
-   Verwenden Sie die bereitgestellten Dienst Informationen (siehe *serviceInfo*), um die neue Basiskonfiguration zu berechnen.
-   Verwenden Sie die bereitgestellten Dienst Informationen (siehe *serviceInfo*) und die Analyse, um die neuen Differenz Informationen zu berechnen.
-   Rufen Sie die Rückruffunktion auf, auf die vom **pfsetinfo** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfsetinfo) verwiesen wird, um die neue Basiskonfiguration in der Sicherheitsdatenbank festzulegen.
-   Rufen Sie die Rückruffunktion auf, auf die vom **pfsetinfo** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfsetinfo) verwiesen wird, um die neuen Analyse Informationen in der Sicherheitsdatenbank festzulegen.

Weitere Informationen finden Sie unter [Implementieren von scesvsintachmentupdate](implementing-scesvcattachmentupdate.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**scesvc- \_ Rückruf \_ Informationen**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**scesvc- \_ Konfigurations \_ Informationen**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




