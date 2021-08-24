---
description: Die IExtender-Schnittstelle stellt einen Satz grundlegender Eigenschaften bereit, die der Schnittstelle eines Steuerelements hinzugefügt werden. Programmierer können diese Eigenschaften so verwenden, als ob sie Teil des Steuerelements sind.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: IExtender-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: 75abc6caf0abab25d98152cf9f905fa10fdd0597b7afda2680639bd8dc9c10b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002040"
---
# <a name="iextender-interface"></a>IExtender-Schnittstelle

Die **IExtender-Schnittstelle** stellt einen Satz grundlegender Eigenschaften bereit, die der Schnittstelle eines Steuerelements hinzugefügt werden. Programmierer können diese Eigenschaften so verwenden, als ob sie Teil des Steuerelements sind.

## <a name="members"></a>Member

Die **IExkeeper-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IExkeeper** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IExtender-Schnittstelle** verfügt über diese Methoden.



| Methode                         | Beschreibung                                    |
|:-------------------------------|:-----------------------------------------------|
| [**Move**](iextender-move.md) | Verschiebt ein MDIForm-, Formular- oder -Steuerelement.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IExtender-Schnittstelle** verfügt über diese Eigenschaften.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Eigenschaft</th>
<th style="text-align: left;">Zugriffstyp</th>
<th style="text-align: left;">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Ausrichten<br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt einen Wert zurück oder legt einen Wert fest, der bestimmt, ob ein Objekt in beliebiger Größe an einer beliebigen Stelle in einem Formular angezeigt wird oder ob es oben, unten, links oder rechts des Formulars angezeigt wird und automatisch so dimensioniert wird, dass es der Breite des Formulars passt.<br/> 
<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vbAlignNone 0</td>
<td>(Standard in einem Nicht-MDI-Formular) Keine– Größe und Position können zur Entwurfszeit oder im Code festgelegt werden. Die Einstellung wird ignoriert, wenn sich das Objekt in einem MDI-Formular befindet.</td>
</tr>
<tr class="even">
<td>vbAlignTop 1</td>
<td>(Standard in einem MDI-Formular) Top: Das -Objekt befindet sich oben im Formular, und seine Breite entspricht der ScaleWidth-Eigenschafteneinstellung des Formulars.</td>
</tr>
<tr class="odd">
<td>vbAlignBottom 2</td>
<td>Unten: Das Objekt befindet sich am unteren Rand des Formulars, und seine Breite entspricht der ScaleWidth-Eigenschafteneinstellung des Formulars.</td>
</tr>
<tr class="even">
<td>vbAlignLeft 3</td>
<td>Links: Das Objekt befindet sich links vom Formular, und seine Breite entspricht der ScaleWidth-Eigenschafteneinstellung des Formulars.</td>
</tr>
<tr class="odd">
<td>vbAlignRight 4</td>
<td>Rechts: Das Objekt befindet sich rechts vom Formular, und seine Breite entspricht der ScaleWidth-Eigenschafteneinstellung des Formulars.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Container</p></td>
<td style="text-align: left;"><p>Schreibgeschützt</p></td>
<td style="text-align: left;"><p>Gibt den Container eines Steuerelements in einem Formular zurück.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Aktiviert</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt einen Wert zurück, der bestimmt, ob ein Formular oder Steuerelement auf vom Benutzer generierte Ereignisse reagieren kann, oder legt diesen fest.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Höhe</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt die Höhe eines Objekts zurück oder legt diese fest.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Hwnd</p></td>
<td style="text-align: left;"><p>Schreibgeschützt</p></td>
<td style="text-align: left;"><p>Gibt ein Handle für ein Formular oder Steuerelement zurück.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Links</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt den Abstand zwischen dem inneren linken Rand eines Objekts und dem linken Rand des Containers zurück oder legt diesen fest.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Name</p></td>
<td style="text-align: left;"><p>Schreibgeschützt</p></td>
<td style="text-align: left;"><p>Gibt den Namen zurück, der im Code zum Identifizieren eines Formulars, Steuerelements oder Datenzugriffsobjekts verwendet wird.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Parent</p></td>
<td style="text-align: left;"><p>Schreibgeschützt</p></td>
<td style="text-align: left;"><p>Gibt das Formular, das Objekt oder die Auflistung zurück, das ein Steuerelement oder ein anderes Objekt oder eine andere Auflistung enthält.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Tabstop</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt einen Wert zurück, der angibt, ob ein Benutzer die <strong>TAB-TASTE</strong> verwenden kann, um einem Objekt den Fokus zu geben, oder legt diesen fest.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Oben</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt den Abstand zwischen dem inneren oberen Rand eines Objekts und dem oberen Rand des Containers zurück oder legt diesen fest.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Sichtbar</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt einen Wert zurück, der angibt, ob ein Objekt sichtbar oder ausgeblendet ist, oder legt diesen fest.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Breite</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt die Breite eines Objekts zurück oder legt diese fest.</p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



 

 
