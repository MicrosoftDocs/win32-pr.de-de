---
title: IADsOctetList-Eigenschaftsmethoden (Iads.h)
description: Die -Eigenschaftsmethode der IADsOctetList-Schnittstelle legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter Schnittstelleneigenschaftsmethoden.
ms.assetid: 6fe29a0d-dd53-4cc2-8152-22a0a2756c2c
ms.tgt_platform: multiple
keywords:
- IADsOctetList-Eigenschaftenmethoden ADSI
topic_type:
- apiref
api_name:
- IADsOctetList Property Methods
- IADsOctetList.OctetList
- IADsOctetList.get_OctetList
- IADsOctetList.put_OctetList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa434eaf9cde95adb4b43d0261ac779d5183d9f3de2284704bc75cfa564521e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023438"
---
# <a name="iadsoctetlist-property-methods"></a>IADsOctetList-Eigenschaftenmethoden

Die -Eigenschaftsmethode der [**IADsOctetList-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**OctetList**
</dt> <dd> <dl>

Eine geordnete Sequenz von Bytearrays.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetList(
  [out] VARIANT* retVal
);
HRESULT put_OctetList(
  [in] VARIANT vOctetList
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
| IID<br/>                      | IID \_ IADsOctetList ist als 7B28B80F-4680-11D1-A3B4-00C04FB950DC definiert.<br/>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)
</dt> <dt>

[**ADS \_ OCTET \_ LIST**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)
</dt> </dl>

 

 





