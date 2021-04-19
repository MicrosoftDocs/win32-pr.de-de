---
description: 'Weitere Informationen über: Windows8Api. JetOpenTemporaryTable2-Methode'
title: Windows8Api. JetOpenTemporaryTable2-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetOpenTemporaryTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetopentemporarytable2(v=EXCHG.10)
ms:contentKeyID: 55107829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ebb96af18e655c9f9304e2fe7a339663c0206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360113"
---
# <a name="windows8apijetopentemporarytable2-method"></a>Windows8Api. JetOpenTemporaryTable2-Methode

Erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird. Siehe auch [jetopentemptable (JET_SESID, \[ \] , Int32, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), "API. JetOpenTempTable2", [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md). [Jetopumtemporarytable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable2 ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEWindows8Api.JetOpenTemporaryTable2(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable2(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - temporarytable  
    Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)  
    
    Die Beschreibung der temporären Tabelle, die bei der Eingabe erstellt werden soll. Nach einem erfolgreichen-Vorgang enthält die-Struktur das Handle für die temporären Tabellen-und Spalten Identifizierungen. Verwenden Sie [jetclosetable (JET_SESID JET_TABLEID)](./api.jetclosetable-method.md) , um die temporäre Tabelle zu verwenden, wenn Sie fertig sind.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [jetopentemporarytable (JET_SESID JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) für frühere Versionen von ESENT.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Windows8Api-Klasse](./windows8api-class.md)

[Windows8Api-Member](./windows8api-members.md)

[Microsoft. ISAM. ESENT. Interop. Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
