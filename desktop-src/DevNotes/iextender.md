---
description: Die IExaufsicht-Schnittstelle stellt eine Reihe von grundlegenden Eigenschaften bereit, die der Schnittstelle eines Steuerelements hinzugefügt werden. Programmierer können diese Eigenschaften so verwenden, als wären sie Teil des Steuerelements.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: IExface-Schnittstelle
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
ms.openlocfilehash: a341f5d8a0ec554f008232f44156486df83d0fd8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625112"
---
# <a name="iextender-interface"></a>IExface-Schnittstelle

Die **IExaufsicht-Schnittstelle** stellt eine Reihe von grundlegenden Eigenschaften bereit, die der Schnittstelle eines Steuerelements hinzugefügt werden. Programmierer können diese Eigenschaften so verwenden, als wären sie Teil des Steuerelements.

## <a name="members"></a>Member

Die **IExune-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IExbat** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IExface-Schnittstelle** verfügt über diese Methoden.



| Methode                         | Beschreibung                                    |
|:-------------------------------|:-----------------------------------------------|
| [**Move**](iextender-move.md) | Verschiebt ein MDIForm-, Formular- oder -Steuerelement.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IExface-Schnittstelle** verfügt über diese Eigenschaften.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Eigenschaft</th>
<th >Zugriffstyp</th>
<th >Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td >Ausrichten<br/></td>
<td >Lesen/Schreiben<br/></td>
<td >Gibt einen Wert zurück oder legt einen Wert fest, der bestimmt, ob ein Objekt in einer beliebigen Größe an einer beliebigen Stelle in einem Formular angezeigt wird oder ob es oben, unten, links oder rechts des Formulars angezeigt wird und automatisch an die Breite des Formulars angepasst wird.<br/> 
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
<td>(Standard in einem Nicht-MDI-Formular) Keine: Größe und Speicherort können zur Entwurfszeit oder im Code festgelegt werden. Die Einstellung wird ignoriert, wenn sich das Objekt in einem MDI-Formular befindet.</td>
</tr>
<tr class="even">
<td>vbAlignTop 1</td>
<td>(Standard in einem MDI-Formular) Top: Das Objekt befindet sich am oberen Rand des Formulars, und seine Breite entspricht der ScaleWidth-Eigenschafteneinstellung des Formulars.</td>
</tr>
<tr class="odd">
<td>vbAlignBottom 2</td>
<td>Unten: Das Objekt befindet sich am unteren Rand des Formulars, und seine Breite entspricht der Eigenschaftseinstellung ScaleWidth des Formulars.</td>
</tr>
<tr class="even">
<td>vbAlignLeft 3</td>
<td>Links: Das -Objekt befindet sich links vom Formular, und seine Breite entspricht der ScaleWidth-Eigenschafteneinstellung des Formulars.</td>
</tr>
<tr class="odd">
<td>vbAlignRight 4</td>
<td>Rechts: Das Objekt befindet sich rechts neben dem Formular, und seine Breite entspricht der Eigenschaftseinstellung ScaleWidth des Formulars.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><p>Container</p></td>
<td ><p>Schreibgeschützt</p></td>
<td ><p>Gibt den Container eines Steuerelements für ein Formular zurück.</p></td>
</tr>
<tr class="odd">
<td ><p>Aktiviert</p></td>
<td ><p>Lesen/Schreiben</p></td>
<td ><p>Gibt einen Wert zurück, der bestimmt, ob ein Formular oder Steuerelement auf vom Benutzer generierte Ereignisse reagieren kann, oder legt diesen fest.</p></td>
</tr>
<tr class="even">
<td ><p>Höhe</p></td>
<td ><p>Lesen/Schreiben</p></td>
<td ><p>Gibt die Höhe eines Objekts zurück oder legt diese fest.</p></td>
</tr>
<tr class="odd">
<td ><p>Hwnd</p></td>
<td ><p>Schreibgeschützt</p></td>
<td ><p>Gibt ein Handle für ein Formular oder Steuerelement zurück.</p></td>
</tr>
<tr class="even">
<td ><p>Left</p></td>
<td ><p>Lesen/Schreiben</p></td>
<td ><p>Gibt den Abstand zwischen dem internen linken Rand eines Objekts und dem linken Rand des Containers zurück oder legt diese fest.</p></td>
</tr>
<tr class="odd">
<td ><p>Name</p></td>
<td ><p>Schreibgeschützt</p></td>
<td ><p>Gibt den Namen zurück, der im Code zum Identifizieren eines Formulars, Steuerelements oder Datenzugriffsobjekts verwendet wird.</p></td>
</tr>
<tr class="even">
<td ><p>Parent</p></td>
<td ><p>Schreibgeschützt</p></td>
<td ><p>Gibt das Formular, das Objekt oder die Auflistung zurück, das ein Steuerelement oder ein anderes Objekt oder eine andere Auflistung enthält.</p></td>
</tr>
<tr class="odd">
<td ><p>Tabstop</p></td>
<td ><p>Lesen/Schreiben</p></td>
<td ><p>Gibt einen Wert zurück, der angibt, ob ein Benutzer die <strong>TAB-TASTE</strong> verwenden kann, um den Fokus auf ein Objekt zu legen, oder legt diesen fest.</p></td>
</tr>
<tr class="even">
<td ><p>Oben</p></td>
<td ><p>Lesen/Schreiben</p></td>
<td ><p>Gibt den Abstand zwischen dem internen oberen Rand eines Objekts und dem oberen Rand des Containers zurück oder legt diese fest.</p></td>
</tr>
<tr class="odd">
<td ><p>Sichtbar</p></td>
<td ><p>Lesen/Schreiben</p></td>
<td ><p>Gibt einen Wert zurück, der angibt, ob ein Objekt sichtbar oder ausgeblendet ist, oder legt diesen fest.</p></td>
</tr>
<tr class="even">
<td ><p>Breite</p></td>
<td ><p>Lesen/Schreiben</p></td>
<td ><p>Gibt die Breite eines Objekts zurück oder legt diese fest.</p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



 

 
