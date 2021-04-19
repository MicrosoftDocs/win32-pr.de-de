---
description: Stellt den Zugriff auf ein Rechteck dar.
ms.assetid: 78e6c29c-0f43-46a5-9d30-948de5f369c8
title: Inkrechteck-Klasse (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRectangle
- InkRectangle.IInkRectangle
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: d643696fe19523bac93ebca71cf885cd93b8570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366307"
---
# <a name="inkrectangle-class"></a>Inkrechteck-Klasse

Stellt den Zugriff auf ein Rechteck dar.

**Inkrechteck** verfügt über folgende Typen von Membern:

-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **inkrechteck** -Klasse definiert.



| Schnittstelle         | BESCHREIBUNG                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **Iinkrechteck** | Dieses Objekt implementiert die **iinkrechteck** -com-Schnittstelle.<br/> |



 

### <a name="methods"></a>Methoden

Die **inkrechteck** -Klasse verfügt über diese Methoden.



| Methode                                            | BESCHREIBUNG                                                                        |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**Getrechteck**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-getrectangle) | Ruft die Elemente des **inkrechteck** -Objekts in einem einzelnen-Befehl ab.<br/> |
| [**Setrechteck**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-setrectangle) | Ändert die Elemente des **inkrechteck** -Objekts in einem einzelnen-Befehl.<br/>  |



 

### <a name="properties"></a>Eigenschaften

Die **inkrechteck** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                         | Zugriffstyp           | BESCHREIBUNG                                                        |
|:-------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**bottom**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)<br/> | Lesen/Schreiben<br/> | Ruft die untere Position des Rechtecks ab oder legt diese fest.<br/>      |
| [**Daten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_data)<br/>     | Lesen/Schreiben<br/> | Ruft den Zugriff auf die Rechteck Struktur ab oder legt ihn fest (nur C++).<br/> |
| [**Linken**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)<br/>     | Lesen/Schreiben<br/> | Ruft die linke Position des Rechtecks ab oder legt diese fest.<br/>        |
| [**Richting**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)<br/>   | Lesen/Schreiben<br/> | Ruft die Rechte Position des Rechtecks ab oder legt diese fest.<br/>       |
| [**Nach oben**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)<br/>       | Lesen/Schreiben<br/> | Ruft die oberste Position des Rechtecks ab oder legt diese fest.<br/>         |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Ein Punkt befindet sich innerhalb eines **inkrechtecks** , wenn es auf der [**linken**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left) oder [**oberen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top) Seite liegt oder sich innerhalb aller vier Seiten befindet. Ein Punkt auf der [**rechten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right) oder [**unteren**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom) Seite wird außerhalb des Rechtecks berücksichtigt.

 

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode instanziiert werden.

> [!Note]  
> Ein **inkrechteck** kann nicht verwendet werden, wenn es größer als Long \_ Max (2 ^ 31-1) in beiden Dimensionen ist.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

