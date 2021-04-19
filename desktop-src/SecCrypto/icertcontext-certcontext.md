---
description: Legt den pccert-Kontext eines Zertifikats fest oder ruft ihn ab \_ .
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'Icertcontext:: certcontext-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361979"
---
# <a name="icertcontextcertcontext-property"></a>Icertcontext:: certcontext-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **certcontext** -Eigenschaft legt den pccert- \_ Kontext eines Zertifikats fest oder ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a>Eigenschaftswert

Der pccert- \_ Kontext des Zertifikats.

## <a name="error-codes"></a>Fehlercodes

Wenn die Eigenschaften Zugriffsmethoden **\_ certcontext platzieren** und **\_ certcontext** erfolgreich abrufen, geben Sie S \_ OK zurück.

Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Sie müssen entweder die [**freecontext**](icertcontext-freecontext.md) -Methode oder die [**certfreecertifitorecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) -Funktion abrufen, um den kontextfrei zugeben.

Wenn Sie die **certcontext** -Eigenschaft festlegen, wird der Status des gesamten [**Zertifikat**](certificate.md) Objekts zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icertcontext**](icertcontext.md)
</dt> </dl>

 

 




