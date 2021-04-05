---
description: Die scesvasetachmentconfig-Funktion wird von der Sicherheitskonfigurations-Engine aufgerufen, wenn das System konfiguriert ist.
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: Scesvcalltachmentconfig-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750872"
---
# <a name="scesvcattachmentconfig-callback-function"></a>Scesvcalltachmentconfig-Rückruffunktion

Die **scesvasetachmentconfig** -Funktion wird von der Sicherheitskonfigurations-Engine aufgerufen, wenn das System konfiguriert ist.

## <a name="syntax"></a>Syntax


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pscecbinfo* \[ in\]
</dt> <dd>

Zeiger auf eine [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur, die das Daten Bank Handle und die Rückruf Funktionen enthält, um Informationen abzufragen, festzulegen und freizugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird "scestatus Success" zurückgegeben \_ . Andernfalls wird ein Fehlercode zurückgegeben. Weitere Informationen zu den Sicherheits Konfigurations-Fehlercodes finden Sie unter [Anhang Return Values](management-return-values.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie bei der Implementierung dieser Funktion die Rückruffunktion, auf die vom **pfqueryinfo** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfqueryinfo) verwiesen wird, um Konfigurationsinformationen abzurufen. Konfigurieren Sie dann den Dienst mithilfe der zurückgegebenen Informationen.

Diese Funktion muss folgende Aktionen ausführen:

-   Abfragen von Konfigurationsinformationen aus dem Sicherheitskonfigurations Tool, die mithilfe der Rückruffunktion festgelegt werden, auf die das **pfqueryinfo** -Element der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur verweist (pscecbinfo->pfqueryinfo).
-   Konfigurieren Sie den Dienst mithilfe der Konfigurationsinformationen.

Weitere Informationen finden Sie unter [Implementieren von scesvsintachmentconfig](implementing-scesvcattachmentconfig.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**scesvc- \_ Rückruf \_ Informationen**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**Scesvpetachmentanalysis**](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




