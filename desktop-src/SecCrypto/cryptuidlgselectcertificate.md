---
description: Zeigt ein Dialogfeld an, in dem Benutzer ein Zertifikat auswählen können.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: CryptUIDlgSelectCertificate-Funktion
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 65d9993cd1e035473e731056d33b7a391ef47b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218187"
---
# <a name="cryptuidlgselectcertificate-function"></a>CryptUIDlgSelectCertificate-Funktion

Die Funktion **cryptuidlgselectcertificate** zeigt ein Dialogfeld an, in dem Benutzer ein Zertifikat auswählen können.

## <a name="syntax"></a>Syntax


```C++
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcsc* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**cryptui \_ selectcertificate \_**](cryptui-selectcertificate-struct.md) -Struktur Struktur, die Informationen über das anzuzeigende Dialogfeld enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein Zeiger auf eine [**CERT- \_ Kontext**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) Struktur, die das vom Benutzer ausgewählte Zertifikat darstellt. Nachdem Sie dieses Zertifikat verwendet haben, müssen Sie diesen Zeiger an die [**certfreecertifiskiecontext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) -Funktion übergeben, um den Verweis Zähler des Zertifikat Kontexts zu verringern.

Wenn der **dwFlags** -Member der *pcsc* -Struktur das **cryptui selectcert-Flag für die \_ \_ Mehrfachauswahl** nicht enthält, bedeutet der Rückgabewert **null** , dass der Benutzer das Dialogfeld geschlossen hat, ohne ein Zertifikat auszuwählen.

Wenn der **dwFlags** -Member der *pcsc* -Struktur das **cryptui selectcert-Flag für die \_ \_ Mehrfachauswahl** enthält, gibt diese Funktion immer **null** zurück. Die ausgewählten Zertifikate sind im Zertifikat Speicher enthalten, der durch das **hselectedcertstore** -Mitglied von *pcsc* repräsentiert wird. Wenn die Anzahl der Zertifikate im Speicher vor und nach dem Aufruf von **cryptuidlgselectcertificate** identisch ist, hat der Benutzer das Dialogfeld geschlossen, ohne Zertifikate auszuwählen.

## <a name="remarks"></a>Bemerkungen

Wenn der **dwFlags** -Member der " [**cryptui \_ selectcertificate \_ struct**](cryptui-selectcertificate-struct.md) "-Struktur auf " **cryptui \_ selectcert \_ Legacy**" festgelegt ist, wird das Dialogfeld "Legacy" angezeigt. Andernfalls wird das aktuelle Zertifikat Auswahl Dialogfeld angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                              |
| Ende des Supports<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                       |
| Bibliothek<br/>                  | <dl> <dt>Cryptui. lib</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>            |
| Unicode- und ANSI-Name<br/>   | **Cryptuidlgselectcertifi| EW** (Unicode) und **cryptuidlgselectcertifi-EA** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**cryptui \_ selectcertificate- \_ Struktur**](cryptui-selectcertificate-struct.md)
</dt> </dl>

�

�




