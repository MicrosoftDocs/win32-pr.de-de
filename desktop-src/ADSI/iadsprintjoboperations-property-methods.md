---
title: IADsPrintJobOperations-Eigenschaftsmethoden (Iads.h)
description: Die Eigenschaftenmethoden der IADsPrintJobOperations-Schnittstelle lesen und schreiben die in der folgenden Tabelle aufgeführten Eigenschaften. Weitere Informationen zu Eigenschaftsmethoden finden Sie unter Schnittstelleneigenschaftenmethoden.
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- IADsPrintJobOperations-Eigenschaftsmethoden ADSI
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
ms.openlocfilehash: 70f337681cb7e75a478000bd06daaac1165edaaaf1cb4255b2890347fbcff7de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691069"
---
# <a name="iadsprintjoboperations-property-methods"></a>IADsPrintJobOperations-Eigenschaftsmethoden

Die Eigenschaftenmethoden der [**IADsPrintJobOperations-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) lesen und schreiben die in der folgenden Tabelle aufgeführten Eigenschaften. Weitere Informationen zu Eigenschaftsmethoden finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**PagesPrinted**
</dt> <dd> <dl>

Enthält die Anzahl der gedruckten Seiten.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **LONG**
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

Enthält die Position dieses Druckauftrags in der Druckwarteschlange.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
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

Enthält den aktuellen Status des Druckauftrags, wie durch einen der [**ADSI Print Job Status Constants-Werte**](adsi-print-job-status-constants.md) angegeben.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

**TimeElapsed**
</dt> <dd> <dl>

Enthält die Anzahl von Millisekunden, die seit dem Start des Druckauftrags verstrichen sind.

<dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt, wie die Eigenschaften für [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) verwendet werden können.


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
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsPrintJobOperations ist als 32FB6780-1ED0-11CF-A988-00AA006BC149 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**ADSI Druckauftragsstatuskonstanten**](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





