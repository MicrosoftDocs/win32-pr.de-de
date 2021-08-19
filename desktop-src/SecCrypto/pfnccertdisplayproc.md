---
description: Eine benutzerdefinierte Rückruffunktion, die es dem Aufrufer der CryptUIDlgSelectCertificate-Funktion ermöglicht, die Anzeige von Zertifikaten zu verarbeiten, die der Benutzer zur Anzeige auswählt.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: PFNCCERTDISPLAYPROC-Rückruffunktion
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
ms.openlocfilehash: a0d78569990874c87082d57045cf8075043c6edccc96b507d2d8dc72a58fb379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978976"
---
# <a name="pfnccertdisplayproc-callback-function"></a>PFNCCERTDISPLAYPROC-Rückruffunktion

Die **PFNCCERTDISPLAYPROC-Funktion** ist eine benutzerdefinierte Rückruffunktion, mit der der Aufrufer der [**CryptUIDlgSelectCertificate-Funktion**](cryptuidlgselectcertificate.md) die Anzeige von Zertifikaten verarbeiten kann, die der Benutzer zur Anzeige auswählt.

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

*pCertContext* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CERT \_ CONTEXT-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) die das anzuzeigende Zertifikat darstellt.

</dd> <dt>

*hWndSelCertDlg* \[ In\]
</dt> <dd>

Ein Handle für das Dialogfeld, aus dem das Zertifikat für die Anzeige ausgewählt wurde.

</dd> <dt>

*pvCallbackData* \[ In\]
</dt> <dd>

Zusätzliche Daten, die von der Rückruffunktion verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE zurück,** um anzugeben, dass sie die Anzeige des Zertifikats verarbeitet und dass das Dialogfeld das Zertifikat nicht anzeigen soll. Wenn diese Funktion **FALSE zurückgibt,** zeigt das Dialogfeld das Zertifikat an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



 

 




