---
description: Ruft den Namen der Zertifikat Vorlage ab.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'Iscrdenr:: getcerttemplatename-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217995"
---
# <a name="iscrdenrgetcerttemplatename-method"></a>Iscrdenr:: getcerttemplatename-Methode

Die **getcerttemplatename** -Methode ruft den Namen der Zertifikat Vorlage ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein-Wert, der bestimmt, ob der tatsächliche Name oder der Anzeige Name der Zertifikat Vorlage zurückgegeben wird. Wenn *dwFlags* den \_ \_ \_ \_ anzeigen Amen "Name der Zertifikat Vorlage" aufweisen \_ , wird der Anzeige Name der Zertifikat Vorlage abgerufen. andernfalls wird der tatsächliche Name der Zertifikat Vorlage angezeigt.

</dd> <dt>

*pbstraucerttemplatename* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen der Zertifikat Vorlage zurückgibt, die in der [*Zertifikat Anforderung*](../secgloss/c-gly.md)verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Eine Zeichenfolge, die den Namen der Zertifikat Vorlage darstellt, die in der [*Zertifikat Anforderung*](../secgloss/c-gly.md)verwendet wird.

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Namen der Zertifikat Vorlage nicht durch Aufrufen von [**iscrdenr:: setcerttemplatename**](iscrdenr-setcerttemplatename.md)festlegen, wird der Name standardmäßig auf den Vornamen in der Liste der verfügbaren Zertifikat Vorlagen festgelegt.

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

[**Iscrdenr:: setcerttemplatename**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
