---
title: Iadsacl-Eigenschafts Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadsacl-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: eb4786d7-d366-4924-8255-dc28ea47a246
ms.tgt_platform: multiple
keywords:
- Iadsacl-Eigenschafts Methoden ADSI
topic_type:
- apiref
api_name:
- IADsAcl Property Methods
- IADsAcl.ProtectedAttrName
- IADsAcl.get_ProtecteAttrName
- IADsAcl.put_ProtectedAttrName
- IADsAcl.SubjectName
- IADsAcl.get_SubjectName
- IADsAcl.put_SubjectName
- IADsAcl.Privileges
- IADsAcl.get_Privileges
- IADsAcl.put_Privileges
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d8afb1ba3cbf7749ad8e3d14fa970662715909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478126"
---
# <a name="iadsacl-property-methods"></a>Iadsacl-Eigenschaften Methoden

Die-Eigenschaften Methode der [**iadsacl**](/windows/desktop/api/Iads/nn-iads-iadsacl) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Berechtigungen**
</dt> <dd> <dl>

Berechtigungseinstellungen.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Privileges(
  [out] LONG* retval
);
HRESULT put_Privileges(
  [in] LONG lnPrivileges
);
```


</dt> </dl> </dd> <dt>

**Protectedattrname**
</dt> <dd> <dl>

Name eines geschützten Attributs.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProtecteAttrName(
  [out] BSTR* retVal
);
HRESULT put_ProtectedAttrName(
  [in] BSTR bstrProtectedAttrName
);
```


</dt> </dl> </dd> <dt>

**SubjectName**
</dt> <dd> <dl>

Der Name des Subjekts.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SubjectName(
  [out] BSTR* retval
);
HRESULT put_SubjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadsacl ist als 8452d3ab-0869-11d1-a377-00c04b950 DC definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)
</dt> </dl>

 

 





