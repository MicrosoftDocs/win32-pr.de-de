---
title: Body-Element (showmessagetype)
description: Enthält den Text, der im Textkörper des Meldungs Felds angezeigt werden soll.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Body-Element Taskplaner
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477469"
---
# <a name="body-showmessagetype-element"></a>Body-Element (showmessagetype)

Enthält den Text, der im Textkörper des Meldungs Felds angezeigt werden soll.

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

Das **Body** -Element wird durch den komplexen Typ " [**showmessagetype**](taskschedulerschema-showmessagetype-complextype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                  | Abgeleitet von                                                               | BESCHREIBUNG                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (Aktionsgruppe)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showmessagetype**](taskschedulerschema-showmessagetype-complextype.md) | Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**MessageBody-Eigenschaft von ishowmessageaction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).

Informationen zur Skript Entwicklung finden Sie unter [**showmessageaction. MessageBody**](showmessageaction-messagebody.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





