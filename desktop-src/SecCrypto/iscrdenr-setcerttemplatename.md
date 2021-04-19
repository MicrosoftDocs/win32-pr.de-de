---
description: Gibt den Namen der Zertifikat Vorlage an.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'Iscrdenr:: setcerttemplatename-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 53ba18626a7d2bb703ed4d11953fb4872cf9257c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348641"
---
# <a name="iscrdenrsetcerttemplatename-method"></a>Iscrdenr:: setcerttemplatename-Methode

Die **setcerttemplatename** -Methode gibt den Namen der Zertifikat Vorlage an.

## <a name="syntax"></a>Syntax


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein Wert, der bestimmt, ob der echte Name oder der Anzeige Name der Zertifikat Vorlage festgelegt wird. Wenn *dwFlags* den \_ \_ \_ \_ anzeigen Amen "Name der Zertifikat Vorlage" aufweisen \_ , wird der Anzeige Name der Zertifikat Vorlage festgelegt. Andernfalls wird der echte Name der Zertifikat Vorlage festgelegt.

</dd> <dt>

*bstraucerttemplatename* \[ in\]
</dt> <dd>

Der Name der Zertifikat Vorlage, die in der Zertifikat Anforderung verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="vb"></a>VB

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Namen der Zertifikat Vorlage nicht durch Aufrufen von **iscrdenr:: setcerttemplatename** festlegen, wird der Name standardmäßig auf den Vornamen in der Liste der verfügbaren Zertifikat Vorlagen festgelegt.

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

[**Iscrdenr:: getcerttemplatename**](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




