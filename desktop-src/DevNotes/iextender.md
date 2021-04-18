---
description: Die IExtender-Schnittstelle stellt eine Reihe von grundlegenden Eigenschaften bereit, die der-Schnittstelle eines-Steuer Elements hinzugefügt werden. Programmierer können diese Eigenschaften verwenden, als wären Sie Teil des-Steuer Elements.
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
ms.openlocfilehash: fd600de816889e1c644a0e6074d9b8a97e0ec80c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368302"
---
# <a name="iextender-interface"></a>IExtender-Schnittstelle

Die **IExtender** -Schnittstelle stellt eine Reihe von grundlegenden Eigenschaften bereit, die der-Schnittstelle eines-Steuer Elements hinzugefügt werden. Programmierer können diese Eigenschaften verwenden, als wären Sie Teil des-Steuer Elements.

## <a name="members"></a>Member

Die **IExtender** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IExtender** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iextenderschnittstelle** verfügt über diese Methoden.



| Methode                         | BESCHREIBUNG                                    |
|:-------------------------------|:-----------------------------------------------|
| [**Move**](iextender-move.md) | Verschiebt eine MDIForm, ein Formular oder ein Steuerelement.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **iextenderschnittstelle** verfügt über diese Eigenschaften.



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
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Ausrichten<br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt einen Wert zurück, der bestimmt, ob ein Objekt in einer beliebigen Größe in einem Formular angezeigt wird, oder ob es am oberen, unteren, linken oder rechten Rand des Formulars angezeigt wird und automatisch an die Breite des Formulars angepasst wird, oder legt diesen Wert fest.<br/> 
<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vbalignnone 0</td>
<td>(Standard in einem nicht-MDI-Formular) None – die Größe und der Speicherort können zur Entwurfszeit oder im Code festgelegt werden. Die Einstellung wird ignoriert, wenn sich das Objekt in einem MDI-Formular befindet.</td>
</tr>
<tr class="even">
<td>vbaligntop 1</td>
<td>(Standard in einem MDI-Formular) Top – das Objekt befindet sich oben im Formular, und seine Breite entspricht der ScaleWidth-Eigenschafts Einstellung des Formulars.</td>
</tr>
<tr class="odd">
<td>vbalignbottom 2</td>
<td>Bottom – das Objekt befindet sich am unteren Rand des Formulars, und seine Breite entspricht der ScaleWidth-Eigenschafts Einstellung des Formulars.</td>
</tr>
<tr class="even">
<td>vbalignleft 3</td>
<td>Left – das Objekt befindet sich auf der linken Seite des Formulars, und seine Breite entspricht der ScaleWidth-Eigenschafts Einstellung des Formulars.</td>
</tr>
<tr class="odd">
<td>vbalignright 4</td>
<td>Right – das-Objekt befindet sich rechts vom Formular, und seine Breite entspricht der ScaleWidth-Eigenschafts Einstellung des Formulars.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Container</p></td>
<td style="text-align: left;"><p>Schreibgeschützt</p></td>
<td style="text-align: left;"><p>Gibt den Container eines-Steuer Elements in einem Formular zurück.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Aktiviert</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt einen Wert zurück, der bestimmt, ob ein Formular oder Steuerelement auf benutzergenerierte Ereignisse reagieren kann, oder legt diesen fest.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Höhe</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt die Höhe eines Objekts zurück oder legt diese fest.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>HWND</p></td>
<td style="text-align: left;"><p>Schreibgeschützt</p></td>
<td style="text-align: left;"><p>Gibt ein Handle für ein Formular oder Steuerelement zurück.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Links</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt den Abstand zwischen dem inneren linken Rand eines Objekts und dem linken Rand seines Containers zurück oder legt ihn fest.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Name</p></td>
<td style="text-align: left;"><p>Schreibgeschützt</p></td>
<td style="text-align: left;"><p>Gibt den Namen zurück, der im Code zum Identifizieren eines Formulars, eines Steuer Elements oder eines Datenzugriffs Objekts verwendet wird.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Parent</p></td>
<td style="text-align: left;"><p>Schreibgeschützt</p></td>
<td style="text-align: left;"><p>Gibt das Formular, das Objekt oder die Auflistung zurück, das ein Steuerelement oder ein anderes Objekt oder eine andere Auflistung enthält.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>TabStop</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt einen Wert zurück oder legt einen Wert fest, der angibt, ob ein Benutzer die <strong>Tab</strong> -Taste verwenden kann, um dem Fokus ein Objekt zu übergeben.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Oben</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt den Abstand zwischen dem internen oberen Rand eines Objekts und dem oberen Rand seines Containers zurück oder legt ihn fest.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Sichtbar</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt einen Wert zurück, der angibt, ob ein Objekt sichtbar oder ausgeblendet ist, oder legt diesen fest.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Breite</p></td>
<td style="text-align: left;"><p>Lesen/Schreiben</p></td>
<td style="text-align: left;"><p>Gibt die Breite eines-Objekts zurück oder legt diese fest.</p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



 

 
