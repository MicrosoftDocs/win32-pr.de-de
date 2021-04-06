---
title: IMsRdpClientNonScriptable4 publishercertificatechain (Eigenschaft)
description: Steuert die Herausgeber Zertifikat Kette. Die Kette wird in einer Variante vom Typ VT \_ ByRef gespeichert, die einen Zeiger auf eine Struktur der Zertifikat \_ Ketten \_ Kontext enthält. Weitere Informationen zu VT \_ -ByRef-Strukturen finden Sie unter Variant und VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- Publishercertificatechain-Eigenschaft Remotedesktopdienste
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, publishercertificatechain (Eigenschaft)
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, publishercertificatechain (Eigenschaft)
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, publishercertificatechain-Eigenschaft
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, publishercertificatechain-Eigenschaft
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, publishercertificatechain-Eigenschaft
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, publishercertificatechain-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859034"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a>IMsRdpClientNonScriptable4::P ublishercertificatechain-Eigenschaft

Steuert die Herausgeber Zertifikat Kette. Die Kette wird in einer Variante vom Typ **VT \_ ByRef** gespeichert, die einen Zeiger auf eine Struktur der [**Zertifikat \_ Ketten \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) enthält. Weitere Informationen zu **VT- \_ ByRef** -Strukturen finden Sie unter [Variant und VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a>Eigenschaftswert

Legt die Herausgeber Zertifikat Kette fest. Die Kette wird in einer Variante vom Typ **VT \_ ByRef** gespeichert, die einen Zeiger auf eine Struktur der [**Zertifikat \_ Ketten \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) enthält.

## <a name="error-codes"></a>Fehlercodes

Gibt bei Erfolg **S \_ OK** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

