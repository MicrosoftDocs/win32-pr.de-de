---
title: Iadsnametranslation-Eigenschaften Methoden (IADs. h)
description: Legt die chasereferral-Eigenschaft fest.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- Iadsnametranslation-Eigenschaften Methoden ADSI
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
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956907"
---
# <a name="iadsnametranslate-property-methods"></a>Iadsnametranslation-Eigenschaften Methoden

Die Property-Methode der [**iadsnametranslation**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) -Schnittstelle legt die **chasereferral** -Eigenschaft fest. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Chasereferral**
</dt> <dd> <dl>

Optionen für die Verweis Verfolgung gemäß der Definition in [**ADS \_ Chase \_ referenrals \_ enum**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum). Wenn die verweisverfolgung festgelegt ist, wird die namens Übersetzung für Objekte durchgeführt, die nicht zu diesem Verzeichnis gehören und die von der Verweis Verfolgung zurückgegeben werden.

<dt>

Zugriffstyp: schreibgeschützt
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Bemerkungen

Die verweiserverfolgungs-Optionen gelten nur, wenn Sie [**iadsnametranslation:: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) und [**iadsnametranslation:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)verwenden. Die Funktion ist nicht in [**iadsnametranslation::**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) Stex oder [**iadsnametranslation:: Getex**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)verfügbar.

Die [**iadsnametranslation**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) -Schnittstelle verfügt über eine partielle Implementierung von [**ADS- \_ \_ Verweigerungs verweisen \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) über die **chasereferral** -Eigenschaft. Wenn die **chasereferral** -Eigenschaft auf 0 (null) festgelegt ist, entspricht Sie der Angabe von **ADS- \_ \_ Verweigerungs verweisen \_ nie** (0). Wenn ein Wert ungleich 0 (null) verwendet wird, entspricht er dem Angeben von ADS-verweisverweisverweisen **\_ \_ \_ immer** (0x60). **Iadsnametranslation** implementiert nicht die " **ADS \_ Chase \_ referenrals unter \_ geordnete** (0x20)" oder " **ADS \_ Chase \_ verweirals \_** "-Option "externe (0x40)"-Optionen.

Die Standardeinstellung für die Weiterleitungs Verfolgung ist aktiviert (ADS-verweisverweisverweise **\_ \_ \_ immer**). Ohne eine verweisverfolgung kann eine namens Übersetzung für die Objekte ausgeführt werden, die sich nur auf dem verbundenen Verzeichnisserver befinden. Wenn Sie nicht sicher sind, ob sich das relevante Objekt auf dem angegebenen Server befindet, sollten Sie diese Eigenschaft auf " **ADS \_ Chase- \_ Verweise \_ immer**" festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadsnametranslation ist als B1B272A3-3625-11d1-A3A4-00C04FB950DC definiert.<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Werbung für Werbung- \_ \_ Verweigerungen \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[**Iadsnametranslation:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[**Iadsnametranslation:: Getex**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[**Iadsnametranslation:: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[**Iadsnametranslation::-TeX**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[Schnittstelleneigenschaften Methoden](interface-property-methods.md)
</dt> </dl>

 

 





