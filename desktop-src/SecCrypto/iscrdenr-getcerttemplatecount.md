---
description: Ruft die Anzahl der Zertifikat Vorlagen ab.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: 'Iscrdenr:: getcerttemplatecount-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868208"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a>Iscrdenr:: getcerttemplatecount-Methode

Die **getcerttemplatecount** -Methode ruft die Anzahl der Zertifikat Vorlagen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein-Wert, der bestimmt, ob die Vorlage für Benutzer-oder Computer Zertifikate bestimmt ist. Wenn dieser Wert "SCard \_ ENROLL \_ User \_ CERT \_ Template" (definiert als 1) ist, wird die zurückgegebene Anzahl für Benutzerzertifikat Vorlagen verwendet. Wenn dieser Wert "SCard \_ ENROLL \_ Computer \_ CERT \_ Template" (definiert als 2) ist, wird die zurückgegebene Anzahl für Computer Zertifikat Vorlagen verwendet.

</dd> <dt>

*pdwcerttemplatecount* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **Long** -Wert, der die Anzahl der Zertifikat Vorlagen zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Ein **Long** -Wert, der die Anzahl der Zertifikat Vorlagen darstellt.

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

[**Iscrdenr:: enumcerttemplatename**](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




