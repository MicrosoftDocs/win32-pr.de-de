---
description: Listet die Namen der Zertifikat Vorlagen auf.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: 'Iscrdenr:: enumcerttemplatename-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362687"
---
# <a name="iscrdenrenumcerttemplatename-method"></a>Iscrdenr:: enumcerttemplatename-Methode

Die **enumcerttemplatename** -Methode listet die Namen der Zertifikat Vorlagen auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Der null basierte Index für die enumerationssequenz.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein-Wert, der bestimmt, ob die aufgelistete Zertifikat Vorlage auf Benutzer-oder Computer Zertifikate angewendet wird. Wenn dieser Wert "SCard \_ ENROLL \_ User \_ CERT \_ Template" (definiert als 1) ist, gilt die Enumeration für Benutzerzertifikat Vorlagen. Wenn dieser Wert "SCard \_ ENROLL \_ Computer \_ CERT \_ Template" (definiert als 2) ist, gilt die Enumeration für Computer Zertifikat Vorlagen.

</dd> <dt>

*pbstraucerttemplatename* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen der aufgelisteten Zertifikat Vorlage zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Eine Zeichenfolge, die den Namen der aufgelisteten Zertifikat Vorlage enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscrdenr**](iscrdenr.md)
</dt> <dt>

[**Iscrdenr:: getcerttemplatecount**](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[**Iscrdenr:: getcerttemplatename**](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[**Iscrdenr:: setcerttemplatename**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




