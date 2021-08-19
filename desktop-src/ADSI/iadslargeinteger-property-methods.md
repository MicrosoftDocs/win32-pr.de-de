---
title: IADsLargeInteger-Eigenschaftsmethoden (Iads.h)
description: Die Eigenschaftenmethoden der IADsLargeInteger-Schnittstelle erhalten und legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen finden Sie unter Schnittstelleneigenschaftsmethoden.
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- IADsLargeInteger-Eigenschaftsmethoden ADSI
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
ms.openlocfilehash: 9b46a992accea468b6f3c8a70c7fcfcbe63cf72667c4394c27df273767a387b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023478"
---
# <a name="iadslargeinteger-property-methods"></a>IADsLargeInteger-Eigenschaftenmethoden

Die Eigenschaftenmethoden der [**IADsLargeInteger-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) erhalten und legen die in der folgenden Tabelle beschriebenen Eigenschaften fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**HighPart**
</dt> <dd> <dl>

Der obere Teil der ganzen Zahl.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
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

Der untere Teil der ganzen Zahl.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
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

 

## <a name="remarks"></a>Hinweise

Wenn largeInt vom **LargeInteger-Typ** ist, wird sein Wert gemäß der folgenden Formel durch die Werte **von HighPart** und **LowPart** angegeben.


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a>Beispiele

Im folgenden Visual Basic Codebeispiel wird eine große ganze Zahl auf 43937327281.


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
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsLargeInteger ist als 9068270B-0939-11D1-8BE1-00C04FD8D503 definiert.<br/>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 





