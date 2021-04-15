---
description: 'Weitere Informationen finden Sie hier: setcolumngrbit-Enumeration'
title: Setcolumngrbit-Enumeration
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893f8e79b910a305bf6caccacd2d928e947be693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485227"
---
# <a name="setcolumngrbit-enumeration"></a>Setcolumngrbit-Enumeration

Optionen für jetsetcolumn.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
```

## <a name="members"></a>Member

<table>
<thead>
<tr class="header">
<th></th>
<th>Membername</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Keine</td>
<td>Standardoptionen.</td>
</tr>
<tr class="even">
<td></td>
<td>Appendlv</td>
<td>Diese Option wird zum Anfügen von Daten an eine Spalte vom Typ JET_coltypLongText oder JET_coltypLongBinary verwendet. Das gleiche Verhalten können Sie erreichen, indem Sie die Größe des vorhandenen Long-Werts ermitteln und iblongvalue in psetup angeben. Es ist jedoch einfacher, dieses grbit zu verwenden, da es nicht erforderlich ist, die Größe des vorhandenen Spaltenwerts zu kennen.</td>
</tr>
<tr class="odd">
<td></td>
<td>Overschreitelv</td>
<td>Diese Option wird verwendet, um den vorhandenen Long-Wert durch die neu bereitgestellten Daten zu ersetzen. Wenn diese Option verwendet wird, ist es so, als ob der vorhandene Long-Wert auf 0 (null) festgelegt wurde, bevor die neuen Daten festgelegt werden.</td>
</tr>
<tr class="even">
<td></td>
<td>Revertumdefaultvalue</td>
<td>Diese Option gilt nur für markierte, Spalten mit geringer Dichte oder mehrwertige Spalten. Dies bewirkt, dass die Spalte bei nachfolgenden Spalten Abruf Vorgängen den Standard Spaltenwert zurückgibt. Alle vorhandenen Spaltenwerte werden entfernt.</td>
</tr>
<tr class="odd">
<td></td>
<td>Separatelv</td>
<td>Diese Option wird verwendet, um einen Long-Wert, Spalten vom Typ JET_coltyp zu erzwingen. LONGTEXT oder JET_coltyp. LONGBINARY, das getrennt vom Rest der Daten Satz Daten gespeichert werden soll. Dies tritt normalerweise auf, wenn die Größe des Long-Werts verhindert, dass Sie mit den verbleibenden Daten Satz Daten gespeichert wird. Diese Option kann jedoch verwendet werden, um zu erzwingen, dass der lange Wert separat gespeichert wird. Beachten Sie, dass lange Werte mit einer Größe von vier Bytes, die kleiner als getrennt sind, nicht erzwungen werden können. In solchen Fällen wird die Option ignoriert.</td>
</tr>
<tr class="even">
<td></td>
<td>Sizelv</td>
<td>Diese Option wird verwendet, um den Eingabepuffer als ganzzahlige Anzahl von Bytes zu interpretieren, die als Länge des Long-Werts festgelegt werden, der durch das angegebene ColumnID und ggf. die Sequenznummer in psetinfo- &gt; itagsequence beschrieben wird. Wenn die angegebene Größe größer ist als der vorhandene Spaltenwert, wird die Spalte um 0s erweitert. Wenn die Größe kleiner als der vorhandene Spaltenwert ist, wird der Wert abgeschnitten.</td>
</tr>
<tr class="odd">
<td></td>
<td>Uniquemultivalues</td>
<td>Diese Option wird verwendet, um zu erzwingen, dass alle Werte in einer mehrwertigen Spalte voneinander abweichen. Mit dieser Option werden die Quell Spaltendaten ohne Transformationen mit anderen vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird. Wenn diese Option angegeben ist, können appendlv, overwrite telv und sizelv nicht gleichzeitig angegeben werden.</td>
</tr>
<tr class="even">
<td></td>
<td>UniqueNormalizedMultiValues</td>
<td>Diese Option wird verwendet, um zu erzwingen, dass alle Werte in einer mehrwertigen Spalte voneinander abweichen. Mit dieser Option wird die normalisierte Transformation von Spaltendaten mit anderen ähnlich transformierten vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird. Wenn diese Option angegeben ist, können appendlv, overwrite telv und sizelv nicht gleichzeitig angegeben werden.</td>
</tr>
<tr class="odd">
<td></td>
<td>Nullover</td>
<td>Diese Option wird verwendet, um einen Wert auf die Länge 0 (null) festzulegen. Normalerweise wird ein Spaltenwert auf NULL festgelegt, indem ein cbmax-Wert von 0 (null) übergeben wird. Für einige Typen, wie z. b. JET_coltyp. Text: ein Spaltenwert kann eine Länge von 0 (null) anstelle von NULL sein, und diese Option wird verwendet, um zwischen null und 0 (null) zu unterscheiden.</td>
</tr>
<tr class="even">
<td></td>
<td>Intrinsier-CLV</td>
<td>Versuchen Sie, lange Wert Spalten im Datensatz zu speichern, auch wenn Sie die Standard Trennungs Größe überschreiten.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

[Compressed](./windows7grbits.compressed-field.md)

[Nicht komprimiert](./windows7grbits.uncompressed-field.md)
