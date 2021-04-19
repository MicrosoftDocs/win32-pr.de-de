---
description: Gibt eine hohe, mittlere oder geringe Auswirkung auf ein Gerät an, auf dem ein veralteter Betriebssystem ausgeführt wird.
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: Updateimpactlevel-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372873"
---
# <a name="updateimpactlevel-enumeration"></a>Updateimpactlevel-Enumeration

Gibt eine hohe, mittlere oder geringe Auswirkung auf ein Gerät an, auf dem ein veralteter Betriebssystem ausgeführt wird. Diese Enumeration wird in der Regel von [**updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) -Strukturen verwendet, die wiederum innerhalb des zurückgegebenen [**osupdateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) -Werts von [**gedesupdateassessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment)geschachtelt sind.

## <a name="syntax"></a>Syntax


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**Updateimpactlevel \_ Keine**
</dt> <dd>

Es gibt keine vorhersehbaren Auswirkungen auf Ihr Gerät. Dies kann darauf zurückzuführen sein, dass das Gerät auf dem neuesten Stand ist oder nicht auf dem neuesten Stand ist, weil das Gerät seine Windows Update für Geschäfts zurückstellungs Zeiträume berücksichtigt oder veraltet ist, aber den **daysouumfdate** -Schwellenwert noch nicht erreicht hat, um eine höhere Auswirkung zu erreichen.

</dd> <dt>

<span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**Updateimpactlevel \_ niedrig**
</dt> <dd>

Auf dem Gerät wird nicht das neueste Betriebssystem, sondern ein aktuellstes Update ausgeführt.

</dd> <dt>

<span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**Updateimpactlevel \_ Mittel**
</dt> <dd>

Auf dem Gerät wird das neueste Betriebssystem ausgeführt, aber es wird ein moderater neueres Update ausgeführt.

</dd> <dt>

<span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**Updateimpactlevel \_ hoch**
</dt> <dd>

Das Gerät ist seit längerer Zeit veraltet. Dieses Gerät weist möglicherweise Sicherheitsrisiken auf und enthält möglicherweise wichtige Korrekturen, mit denen Windows besser ausgeführt werden kann. Wenn auf einem Gerät eine Version von Windows ausgeführt wird, die nicht mehr unterstützt wird, wird **updateimpactlevel \_ High** immer zurückgegeben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn [**gedesupdateassessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) aufgerufen wird, wird eine [**osupdateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) -Struktur zurückgegeben. Innerhalb der-Struktur gibt es einen " **Assessment mentforcurrent** " und " **Assessment mentforuptodate**". Beide sind [**updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) -Strukturen. Beide Member verfügen über eine **updateimpactlevel** -Enumeration, die eine hohe, mittlere, geringe oder keine Auswirkung für ein Gerät mit einem veralteten Betriebssystem angibt. Diese Ebenen werden durch den Wert von **daysoudef Date** bestimmt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                   |
| IDL<br/>                      | <dl> <dt>Waasapi. idl</dt> </dl> |



 

 




