---
title: IADsCaseIgnoreList-Eigenschaftsmethoden (Iads.h)
description: Die -Eigenschaftsmethode der IADsCaseIgnoreList-Schnittstelle legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter Schnittstelleneigenschaftsmethoden.
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- IADsCaseIgnoreList-Eigenschaftsmethoden ADSI
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e2f07d3c4afa6cd55f6a757ccae6f2d1076b954e0afdd0c82c8a5247af33f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961919"
---
# <a name="iadscaseignorelist-property-methods"></a>IADsCaseIgnoreList-Eigenschaftsmethoden

Die -Eigenschaftsmethode der [**IADsCaseIgnoreList-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**CaseIgnoreList**
</dt> <dd> <dl>

Eine geordnete Sequenz von Zeichenfolgen, bei der die Groß-/Kleinschreibung nicht beachtet wird.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsCaseIgnoreList ist als 7B66B533-4680-11D1-A3B4-00C04FB950DC definiert.<br/>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[**ADS \_ CASEIGNORE \_ LIST**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 





