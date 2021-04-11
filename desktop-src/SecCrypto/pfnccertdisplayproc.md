---
description: Eine benutzerdefinierte Rückruffunktion, die es dem Aufrufer der Funktion cryptuidlgselectcertificate ermöglicht, die Anzeige von Zertifikaten zu verarbeiten, die der Benutzer zum anzeigen auswählt.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: Pfnccertdisplayproc-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7371e983b339ff8bfa9edb1b7fb795ab64596a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042319"
---
# <a name="pfnccertdisplayproc-callback-function"></a>Pfnccertdisplayproc-Rückruffunktion

Die **pfnccertdisplayproc** -Funktion ist eine benutzerdefinierte Rückruffunktion, die es dem Aufrufer der Funktion [**cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md) ermöglicht, die Anzeige von Zertifikaten zu verarbeiten, die der Benutzer zum anzeigen auswählt.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcertcontext* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur, die das anzuzeigende Zertifikat darstellt.

</dd> <dt>

*hwndselcertdlg* \[ in\]
</dt> <dd>

Ein Handle für das Dialogfeld, in dem das Zertifikat zum Anzeigen ausgewählt wurde.

</dd> <dt>

*pvcallbackdata* \[ in\]
</dt> <dd>

Zusätzliche Daten, die von der Rückruffunktion verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, um anzugeben, dass Sie die Anzeige des Zertifikats behandelt und dass das Dialogfeld das Zertifikat nicht anzeigen soll. Wenn diese Funktion **false** zurückgibt, wird das Zertifikat im Dialogfeld angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



 

 




