---
title: IADsLargeInteger-Eigenschafts Methoden (IADs. h)
description: Die Eigenschaften Methoden der IADsLargeInteger-Schnittstelle erhalten und legen die Eigenschaften fest, die in der folgenden Tabelle beschrieben werden. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- Iadslargeingeteger-Eigenschafts Methoden ADSI
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 097e9ae7387658f983c691e56e4f90ba40dea407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340001"
---
# <a name="iadslargeinteger-property-methods"></a>Iadslargeingeteger-Eigenschaften Methoden

Die Eigenschaften Methoden der [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) -Schnittstelle erhalten und legen die Eigenschaften fest, die in der folgenden Tabelle beschrieben werden. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**HighPart**
</dt> <dd> <dl>

Der hohe Teil der Ganzzahl.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

**LowPart**
</dt> <dd> <dl>

Der niedrige Teil der Ganzzahl.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Bemerkungen

Wenn largeint den **LargeInteger** -Typ aufweist, wird der Wert von den Werten von **highpart** und **LowPart** gemäß der folgenden Formel angegeben.


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a>Beispiele

Im folgenden Visual Basic Codebeispiel wird eine große Ganzzahl auf 43937327281 festgelegt.


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsLargeInteger ist definiert als 9068270b-0939-11d1-8be1-00c04sd8d503<br/>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 





