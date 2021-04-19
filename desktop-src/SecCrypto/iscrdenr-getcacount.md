---
description: Gibt die Anzahl der Zertifizierungsstellen (CAS) zurück, die bereit sind, ein Zertifikat basierend auf der angegebenen Zertifikat Vorlage auszustellen.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'Iscrdenr:: getcacount-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364222"
---
# <a name="iscrdenrgetcacount-method"></a>Iscrdenr:: getcacount-Methode

Die **getcacount** -Methode gibt die Anzahl der [*Zertifizierungs*](../secgloss/c-gly.md) stellen (CAS) zurück, die bereit sind, ein Zertifikat basierend auf der angegebenen Zertifikat Vorlage auszustellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstraucerttemplatename* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die den Namen der Zertifikat Vorlage darstellt.

</dd> <dt>

*pdwcacount* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **Long** -Wert, der die Anzahl der verfügbaren CAS zurückgibt, die ein Zertifikat für die in *bstrincerttemplatename* angegebene Zertifikat Vorlage ausstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Ein **langer** Wert, der die Anzahl der verfügbaren Zertifizierungsstellen darstellt, die ein Zertifikat für die in *bstrincerttemplatename* angegebene Zertifikat Vorlage ausstellen.

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

[**Iscrdenr:: enumcaname**](iscrdenr-enumcaname.md)
</dt> <dt>

[**Iscrdenr:: getcaname**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
