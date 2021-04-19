---
title: TITLEBAR_TYPE-Enumeration (Software-Domänen Controller. h)
description: Elemente der Titlebar- \_ Typenumeration werden verwendet, um die Typen von titlebars anzugeben, die für ein weiches Tastatur Fenster verfügbar sind.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- TITLEBAR_TYPE Enumeration Text Services-Framework
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342016"
---
# <a name="titlebar_type-enumeration"></a>TitleBar- \_ Typenumeration

Elemente der **TitleBar- \_ Typenumeration** werden verwendet, um die Typen von titlebars anzugeben, die für ein weiches Tastatur Fenster verfügbar sind.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TitleBar \_ None**
</dt> <dd>

Das weiche Tastatur Fenster verwendet keine Titlebar.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**nur Titlebar- \_ \_ gripperhoriz \_**
</dt> <dd>

Das weiche Tastatur Fenster verwendet nur eine horizontale Zieh Punkt Leiste.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TitleBar-Zieh Punkt \_ \_ nur Verti \_**
</dt> <dd>

Das weiche Tastatur Fenster verwendet nur eine vertikale Zieh Punkt Leiste.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**TitleBar- \_ gripperschaltfläche \_**
</dt> <dd>

Das weiche Tastatur Fenster verwendet nur eine Zieh Punkt Schaltfläche.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Software-Domänen Controller. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Software. idl</dt> </dl> |



 

 





