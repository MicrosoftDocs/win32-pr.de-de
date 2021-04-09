---
title: Iadsprintjoboperations-Eigenschaften Methoden (IADs. h)
description: Die Eigenschaften Methoden der iadsprintjoboperations-Schnittstelle lesen und schreiben die in der folgenden Tabelle aufgeführten Eigenschaften. Weitere Informationen zu Eigenschafts Methoden finden Sie unter Interface Property Methods.
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- Iadsprintjoboperations-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2981fcdd8043c0eb0ee8b05cfd0331fe3abfabe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859114"
---
# <a name="iadsprintjoboperations-property-methods"></a>Iadsprintjoboperations-Eigenschaften Methoden

Die Eigenschaften Methoden der [**iadsprintjoboperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) -Schnittstelle lesen und schreiben die in der folgenden Tabelle aufgeführten Eigenschaften. Weitere Informationen zu Eigenschafts Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**PagesPrinted**
</dt> <dd> <dl>

Enthält die Anzahl der gedruckten Seiten.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

**Position**
</dt> <dd> <dl>

Enthält die Position dieses Druckauftrags in der Druck Warteschlange.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

**Status**
</dt> <dd> <dl>

Enthält den aktuellen Status des Druckauftrags, wie durch einen der [**ADSI Print Job-Status Konstanten**](adsi-print-job-status-constants.md) Werte angegeben.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

**Verstrichene Zeit**
</dt> <dd> <dl>

Enthält die Anzahl der Millisekunden, die seit dem Start des Druckauftrags verstrichen sind.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie die Eigenschaften für [**iadsprintjoboperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) verwendet werden können.


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ iadsprintjoboperations ist als 32fb6780-1ed0-11CF-A988-00aa006bc149 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadsprintjob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[**Iadsprintjoboperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[**Iadsprintqueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**Status Konstanten für den ADSI-Druckauftrag**](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





