---
title: IADsNameTranslate-Eigenschaftsmethoden (Iads.h)
description: Legt die Eigenschaft "Referral" fest.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- IADsNameTranslate-Eigenschaftenmethoden ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3993c3f3680dca46d2f880705fae44812a3bb5fd7a046084c1d818c3433ea7f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082384"
---
# <a name="iadsnametranslate-property-methods"></a>IADsNameTranslate-Eigenschaftenmethoden

Die -Eigenschaftsmethode der [**IADsNameTranslate-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) legt die **Eigenschaft "IaDsNameTranslate"** fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Ungnungsreferenz**
</dt> <dd> <dl>

Optionen der Empfehlungsergierung, wie in [**ADS \_ REFERRAL \_ REFERRALS \_ ENUM definiert.**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) Wenn die Verweisübersetzung festgelegt ist, erfolgt die Namensübersetzung für Objekte, die nicht zu diesem Verzeichnis gehören, und sind die Empfehlungen, die von der Empfehlungsübersetzung zurückgegeben werden.

<dt>

Zugriffstyp: Nur Schreibzugriff
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Hinweise

Die Optionen für die Empfehlungsnachfolge gelten nur, wenn Sie [**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) und [**IADsNameTranslate::Get verwenden.**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get) Das Feature ist mit [**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) oder [**IADsNameTranslate::GetEx nicht verfügbar.**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)

Die [**IADsNameTranslate-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) verfügt über eine Partimplementierung von [**ADS ADS ADS \_ \_ REFERRALS \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) über die Eigenschaft "IaDsNameTranslate".  Wenn die **Eigenschaft "AdsReferral"** auf 0 (null) festgelegt ist, ist sie identisch mit der Angabe von **ADS ADS ADS \_ \_ REFERRALS \_ NEVER** (0). Wenn ein Wert ungleich 0 (null) verwendet wird, ist er identisch mit der Angabe von **ADS \_ REFERRAL \_ REFERRALS \_ ALWAYS** (0x60). **IADsNameTranslate** implementiert nicht die **OPTIONEN ADS REFERRAL \_ \_ REFERRALS \_ SUBORDINATE** (0x20) oder **ADS ADS ADS \_ \_ REFERRALS \_ EXTERNAL** (0x40).

Die Standardeinstellung für die Empfehlungsverringerung ist aktiviert **(ADS \_ REFERRAL \_ REFERRALS \_ ALWAYS**). Ohne Verweisübersetzung können Sie die Namensübersetzung nur für die Objekte ausführen, die sich auf dem verbundenen Verzeichnisserver befinden. Wenn Sie nicht sicher sind, ob sich das objekt von Interesse auf dem angegebenen Server befindet, sollten Sie diese Eigenschaft auf **ADS \_ ADS ADS \_ REFERRALS ALWAYS \_ festlegen.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNameTranslate ist als B1B272A3-3625-11D1-A3A4-00C04FB950DC definiert.<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ADS \_ CHASE \_ REFERRALS \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[Schnittstelleneigenschaftsmethoden](interface-property-methods.md)
</dt> </dl>

 

 





