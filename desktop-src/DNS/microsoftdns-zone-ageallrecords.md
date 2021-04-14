---
title: AgeAllRecords-Methode der MicrosoftDNS_Zone-Klasse
description: Die AgeAllRecords-Methode ermöglicht die Alterung einiger oder aller nicht-NS-und nicht-SOA-Datensätze in einer Zone.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- AgeAllRecords-Methode (DNS)
- AgeAllRecords-Methode, DNS, MicrosoftDNS_Zone-Klasse
- MicrosoftDNS_Zone-Klasse DNS, AgeAllRecords-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478477"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a>AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse

Die **AgeAllRecords** -Methode ermöglicht die Alterung einiger oder aller nicht-NS-und nicht-SOA-Datensätze in einer Zone.

## <a name="syntax"></a>Syntax


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NodeName* \[ in, optional\]
</dt> <dd>

Der Name des zu Age enden Knotens.

</dd> <dt>

*ApplyTo subtree* \[ in, optional\]
</dt> <dd>

Gibt an, ob die Alterung auf alle Datensätze in der Teilstruktur angewendet werden soll. Legen Sie diese Einstellung auf true fest, um das Aging auf alle Datensätze in der Teilstruktur anzuwenden, beginnend mit nodename.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Fehler \_ Erfolg gibt an, dass die Alterung erfolgreich abgeschlossen wurde. Jeder andere Wert ist ein Fehlercode.

## <a name="remarks"></a>Bemerkungen

Wenn *NodeName* nicht angegeben wird, unterliegen alle Datensätze der Alterung und der Löschung.

Wenn *NodeName* angegeben wird und *applytsubtree* nicht angegeben oder auf 0 (null) festgelegt ist, werden die Datensätze an dem angegebenen Knoten in den Alterungs-und absteigenden Knoten unterteilt.

Wenn *NodeName* angegeben wird und *ApplyTo Teilstruktur* auf 1 festgelegt ist, werden alle Datensätze der Teilstruktur, beginnend bei *NodeName* , in den Alterungs-und absteigenden Datensätze unterteilt. Der Zeitstempel wird auf die aktuelle Zeit für alle nicht-NS-und nicht-SOA-RRS mit den von den Eingabe Parametern identifizierten Besitzer Namen festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS- \_ Zone**](microsoftdns-zone.md)
</dt> <dt>

[**Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





