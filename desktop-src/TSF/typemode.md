---
title: Typemode-Enumeration (Software-BDC. h)
description: Elemente der typemode-Enumeration werden verwendet, um typmodi anzugeben, die für eine weiche Tastatur verfügbar sind.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- Typemode-Enumeration Text Services-Framework
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340315"
---
# <a name="typemode-enumeration"></a>Typemode-Enumeration

Elemente der **typemode** -Enumeration werden verwendet, um typmodi anzugeben, die für eine weiche Tastatur verfügbar sind.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**Clickmouse**
</dt> <dd>

Der Benutzer kann auf die Bildschirmtasten klicken, um Text einzugeben.

</dd> <dt>

<span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Hocker**
</dt> <dd>

Der Benutzer kann für einen vordefinierten Zeitraum auf einen Schlüssel zeigen, und das ausgewählte Zeichen wird automatisch eingegeben.

</dd> <dt>

<span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**DAT**
</dt> <dd>

Die weiche Tastatur scannt den Eingabebereich ständig und hebt Regionen hervor, in denen der Benutzer eine Tastenkombination drücken oder ein Switch-Input-Gerät verwenden kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Software-Domänen Controller. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Software. idl</dt> </dl> |



 

 





