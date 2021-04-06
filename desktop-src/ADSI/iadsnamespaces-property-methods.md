---
title: Iadsnamespaces-Eigenschaften Methoden (IADs. h)
description: Die Eigenschaften Methoden der iadsnamespaces-Schnittstelle erhalten und legen die Eigenschaften fest, die in der folgenden Tabelle beschrieben werden. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- Iadsnamespaces-Eigenschaften Methoden ADSI
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
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742696"
---
# <a name="iadsnamespaces-property-methods"></a>Iadsnamespaces-Eigenschaften Methoden

Die Eigenschaften Methoden der [**iadsnamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) -Schnittstelle erhalten und legen die Eigenschaften fest, die in der folgenden Tabelle beschrieben werden. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**DefaultContainer**
</dt> <dd> <dl>

Die **defaultcontainer** -Eigenschaft identifiziert ein Basis Container Objekt, das Sie binden und als Ausgangspunkt beim Durchsuchen verwenden können. Diese Daten werden gespeichert und aus dem folgenden Registrierungs Wert abgerufen.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

ADSI definiert die **defaultcontainer** -Eigenschaft, um eine schnelle Möglichkeit zum Erstellen eines Zeigers auf ein zuvor definiertes ADSI-Container Objekt zu erhalten.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

 

## <a name="remarks"></a>Bemerkungen

Anbieter müssen diese Eigenschaft auf Benutzerbasis bereitstellen. Der Standardcontainer wird unmittelbar nach dem Aufruf von **iadsnamespaces festgelegt::p UT \_ defaultcontainer**. Der Aufruf von " [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) *" ist nicht erforderlich. Tatsächlich gibt das vom System bereitgestellte Namespaces-Objekt **E \_ notimpl** für die **IADs. SetInfo** -Methode zurück, die für dieses Objekt aufgerufen wird. Wenn ein Container das Namespaces-Objekt ist, führt ein Enumerationsvorgang immer zu einer Liste von anbieterspezifischen Namespace-Objekten. Wenn [**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) zum Abrufen eines Namespace Objekts verwendet wird, wird der *bstrinclass* -Parameter ignoriert. Dies liegt daran, dass der Container, d. h. das Namespaces-Objekt, nur einen Objekttyp enthält, nämlich anbieterspezifische Namespace Objekte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadsnamespaces ist als 28b96ba0-B330-11CF-A9ad-00aa006bc149 definiert.<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[**Iadsnamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[Schnittstelleneigenschaften Methoden](interface-property-methods.md)
</dt> </dl>

 

 





