---
description: 'Weitere Informationen zu: EnumerateColumnsGrbit-Enumeration'
title: EnumerateColumnsGrbit-Enumeration
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1e6f768d2f8a837416540bcd3ca31f8984e55ad
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466807"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>EnumerateColumnsGrbit-Enumeration

Optionen für JetEnumerateColumns.

Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a>Member


|  | Membername | Beschreibung | 
|--|-------------|-------------|
|  | Keine | Standardoptionen. | 
|  | EnumerateCompressOutput | Beim Auflisten von Spaltenwerten können alle Spalten, für die wir alle Werte abrufen und die nur einen Spaltenwert ungleich NULL aufweisen, in einem komprimierten Format zurückgegeben werden. Der Status für solche Spalten wird auf <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> festgelegt, und die Größe des Spaltenwerts und der Arbeitsspeicher, der den Spaltenwert enthält, werden direkt in der <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN-Struktur</a> zurückgegeben. Es ist nicht garantiert, dass alle berechtigten Spalten auf diese Weise komprimiert werden. Weitere Informationen finden <a href="dn335081(v=exchg.10).md">Sie unter JET_ENUMCOLUMN.</a> | 
|  | EnumerateCopy | Diese Option gibt an, dass die geänderten Spaltenwerte des Datensatzes anstatt der ursprünglichen Spaltenwerte aufgeführt werden sollen. Wenn ein Spaltenwert nicht geändert wurde, wird der ursprüngliche Spaltenwert aufzählt. Auf diese Weise kann ein Spaltenwert, der noch nicht eingefügt oder aktualisiert wurde, beim Einfügen oder Aktualisieren eines Datensatzes aufzählt werden.<p>Diese Option ist identisch mit <a href="hh578120(v=exchg.10).md">RetrieveCopy.</a></p> | 
|  | EnumerateIgnoreDefault | Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist, wird kein Spaltenwert zurückgegeben. Normalerweise wird in diesem Fall der Standardwert für die Spalte zurückgegeben, sofern vorhanden. Wenn die Spalte auf einen anderen Wert als den Standardwert festgelegt ist, wird garantiert, dass ein anderer Wert zurückgegeben wird (wenn also eine Spalte mit einem Standardwert explizit auf NULL festgelegt ist, wird ein NULL-Wert als Wert für diese Spalte zurückgegeben). Auch wenn diese Option angefordert wird, ist es weiterhin möglich, einen Spaltenwert anzuzeigen, der dem Standardwert entspricht. Es wird nicht versucht, Spaltenwerte zu entfernen, die ihren Standardwerten entsprechen. Beachten Sie, dass sich diese Option auf die Ausgabe von <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit) auswirkt,</a> wenn sie mit EnumeratePresenceOnly oder EnumerateTaggedOnly verwendet wird. | 
|  | EnumeratePresenceOnly | Wenn für die angeforderte Spalte oder den Spaltenwert ein Wert ungleich NULL vorhanden ist, werden die zugeordneten Daten nicht zurückgegeben. Stattdessen wird der zugeordnete Status für diese Spalte oder diesen Spaltenwert auf <a href="hh557250(v=exchg.10).md">ColumnPresent</a>festgelegt. Wenn der Spaltenwert NULL ist, wird <a href="hh557250(v=exchg.10).md">ColumnNull</a> wie gewohnt zurückgegeben. | 
|  | EnumerateTaggedOnly | Beim Auflisten aller Spaltenwerte im Datensatz (z. B. wenn numColumnids 0 (null) ist), werden nur markierte Spaltenwerte zurückgegeben. Diese Option ist beim Auflisten eines bestimmten Arrays von Spalten-IDs nicht zulässig. | 



## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

[EnumerateIgnoreUserDefinedDefault](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[EnumerateInRecordOnly](./windows7grbits.enumerateinrecordonly-field.md)
