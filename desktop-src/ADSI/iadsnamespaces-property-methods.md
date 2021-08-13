---
title: IADsNamespaces-Eigenschaftsmethoden (Iads.h)
description: Die IADsNamespaces-Schnittstelleneigenschaftsmethoden erhalten und legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen finden Sie unter Schnittstelleneigenschaftenmethoden.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- IADsNamespaces-Eigenschaftsmethoden ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8daeed67202add437ee06b9905cbd70a0c202863c476155216f2340be1c7b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691428"
---
# <a name="iadsnamespaces-property-methods"></a>IADsNamespaces-Eigenschaftsmethoden

Die [**IADsNamespaces-Schnittstelleneigenschaftsmethoden**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) erhalten und legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**DefaultContainer**
</dt> <dd> <dl>

Die **DefaultContainer-Eigenschaft** identifiziert ein Basiscontainerobjekt, an das Sie beim Durchsuchen binden und als Ausgangspunkt verwenden können. Diese Daten werden gespeichert und aus dem folgenden Registrierungswert abgerufen.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

ADSI definiert die **DefaultContainer-Eigenschaft,** um schnell einen Zeiger auf ein zuvor definiertes ADSI-Containerobjekt zu erhalten.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Hinweise

Anbieter müssen diese Eigenschaft pro Benutzer bereitstellen. Der Standardcontainer wird unmittelbar nach dem Aufruf von **IADsNamespaces::p ut \_ DefaultContainer** festgelegt. Das Aufrufen von [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) ist nicht erforderlich. Tatsächlich gibt das vom System bereitgestellte Namespaceobjekt **E \_ NOTIMPL** für die **IADs.SetInfo-Methode** zurück, die für dieses Objekt aufgerufen wird. Wenn ein Container das Namespaceobjekt ist, führt ein Enumerationsvorgang immer zu einer Liste anbieterspezifischer Namespaceobjekte. Wenn [**IADsContainer.GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) zum Abrufen eines Namespaceobjekts verwendet wird, wird der *bstrClass-Parameter* ignoriert. Dies liegt daran, dass der Container, d. h. das Namespaceobjekt, nur einen Objekttyp enthält, nämlich anbieterspezifische Namespaceobjekte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNamespaces ist als 28B96BA0-B330-11CF-A9AD-00AA006BC149 definiert.<br/>       |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IADsContainer.GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[Schnittstelleneigenschaftsmethoden](interface-property-methods.md)
</dt> </dl>

 

 





