---
description: Zeigt ein Dialogfeld an, in dem ein Benutzer ein Zertifikat auswählen kann.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: CryptUIDlgSelectCertificate-Funktion
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: fb37eb664841331ce3f37e9ce37ca3ab9e5c0f92c254cff0896c6c682a9f2872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768163"
---
# <a name="cryptuidlgselectcertificate-function"></a>CryptUIDlgSelectCertificate-Funktion

Die **CryptUIDlgSelectCertificate-Funktion** zeigt ein Dialogfeld an, in dem ein Benutzer ein Zertifikat auswählen kann.

## <a name="syntax"></a>Syntax


```C++
PCCERT_CONTEXT WINAPI CryptUIDlgSelectCertificate(
  _In_  PCCRYPTUI_SELECTCERTIFICATE_STRUCT pcsc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcsc* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CRYPTUI \_ SELECTCERTIFICATE-STRUKTUR, \_**](cryptui-selectcertificate-struct.md) die Informationen über das anzuzeigende Dialogfeld enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein Zeiger auf eine [**CERT \_ CONTEXT-Struktur,**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) die das vom Benutzer ausgewählte Zertifikat darstellt. Wenn Sie mit der Verwendung dieses Zertifikats fertig sind, müssen Sie diesen Zeiger an die [**CertFreeCertificateContext-Funktion**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) übergeben, um den Verweiszähler des Zertifikatkontexts zu dekrementieren.

Wenn der **dwFlags-Member** der *pcsc-Struktur* das **CRYPTUI \_ SELECTCERT \_ MULTISELECT-Flag** nicht enthält, bedeutet ein Rückgabewert von **NULL,** dass der Benutzer das Dialogfeld geschlossen hat, ohne ein Zertifikat auszuwählen.

Wenn der **dwFlags-Member** der *pcsc-Struktur* das **CRYPTUI \_ SELECTCERT \_ MULTISELECT-Flag** enthält, gibt diese Funktion immer **NULL** zurück. Die ausgewählten Zertifikate werden im Zertifikatspeicher enthalten sein, der durch das **hSelectedCertStore-Element** von *pcsc* dargestellt wird. Wenn die Anzahl der Zertifikate im Speicher vor und nach dem Aufruf von **CryptUIDlgSelectCertificate** gleich ist, hat der Benutzer das Dialogfeld geschlossen, ohne Zertifikate auszuwählen.

## <a name="remarks"></a>Hinweise

Wenn der **dwFlags-Member** der [**CRYPTUI \_ SELECTCERTIFICATE-Struktur \_**](cryptui-selectcertificate-struct.md) auf **CRYPTUI \_ SELECTCERT \_ LEGACY** festgelegt ist, wird das Legacydialogfeld angezeigt. Andernfalls wird das aktuelle Dialogfeld für die Zertifikatauswahl angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows \[ XP-Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                              |
| Ende des Supports<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                       |
| Bibliothek<br/>                  | <dl> <dt>Cryptui.lib</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>            |
| Unicode- und ANSI-Name<br/>   | **CryptUIDlgSelectCertificateW** (Unicode) und **CryptUIDlgSelectCertificateA** (ANSI)<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CRYPTUI \_ \_ SELECTCERTIFICATE-STRUKTUR**](cryptui-selectcertificate-struct.md)
</dt> </dl>






