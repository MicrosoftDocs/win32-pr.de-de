---
title: Ideliveryoptimizationjob ADDFILEWITHRANGES-Methode (deliveryoptimization. h)
description: Fügt einem Download Auftrag eine Datei hinzu und gibt die Bereiche der Datei an, die Sie herunterladen möchten.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- ADDFILEWITHRANGES-Methode
- ADDFILEWITHRANGES-Methode, ideliveryoptimizationjob-Schnittstelle
- Ideliveryoptimizationjob-Schnittstelle, ADDFILEWITHRANGES-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341037"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a>Ideliveryoptimizationjob:: ADDFILEWITHRANGES-Methode

Fügt einem Download Auftrag eine Datei hinzu und gibt die Bereiche der Datei an, die Sie herunterladen möchten.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

nicht im  \[ in\]
</dt> <dd>

Eine NULL beendete Zeichenfolge, die ein eindeutiger Bezeichner für den veröffentlichten Inhalt ist. Bei nicht veröffentlichten Inhalten kann dies eine beliebige eindeutige Zeichenfolge sein, mit der der Aufrufer Dateien innerhalb eines Auftrags identifizieren kann.

</dd> <dt>

*RemoteURL* \[ in\]
</dt> <dd>

Eine auf NULL endenden Zeichenfolge, die den Namen der Datei auf dem Server enthält.

</dd> <dt>

*localname* \[ in\]
</dt> <dd>

Eine auf NULL endenden Zeichenfolge, die den Namen der Datei auf dem Client enthält.

</dd> <dt>

*rangecount* \[ in, optional\]
</dt> <dd>

Anzahl der Elemente in *Bereichen*.

</dd> <dt>

*Bereiche* \[ in, optional\]
</dt> <dd>

Array aus mindestens einer [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) -Struktur, die die Bereiche angeben, die heruntergeladen werden sollen. Geben Sie keine doppelten oder überlappenden Bereiche an.

</dd> <dt>

*FileSize* \[ in, optional\]
</dt> <dd>

Die Länge der Datei in Bytes. Übergeben Sie **DO_UNKNOWN_FILE_SIZE** , wenn die Größe der aufruferanwendung nicht bekannt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden Rückgabewerte als auch andere zurück.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong><strong>S_OK</strong></strong></dt> </dl></td>
<td>Erfolg.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> </dl></td>
<td>Der lokale Dateiname ist NULL oder eine leere Zeichenfolge. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>E_ACCESSDENIED</strong></dt> </dl></td>
<td>Der Benutzer verfügt nicht über die Berechtigung zum Schreiben in das angegebene Verzeichnis auf dem Client.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_RANGE</strong></dt> </dl></td>
<td>Einer der Bereiche ist ungültig. Beispielsweise ist initialoffset auf <strong>BG_LENGTH_TO_EOF</strong>festgelegt.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </dl></td>
<td>Doppelte oder überlappende Bereiche können nicht angegeben werden. <br/>
<blockquote>
[!Note]<br />
Die Bereiche werden nach dem Offset des Werts sortiert, nicht nach der Länge. Wenn Bereiche eingegeben werden, die den gleichen Offset aufweisen, aber in umgekehrter Reihenfolge sind, wird dieser Fehler zurückgegeben. Wenn z. b. 100,5 und 100,0 in dieser Reihenfolge eingegeben werden, können Sie die Datei nicht dem Auftrag hinzufügen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_STATE</strong></dt> </dl></td>
<td>Der Status des Auftrags kann nicht <strong>BG_JOB_STATE_CANCELLED</strong> oder <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>sein.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob ist als EE2584CF-A69C-4848-B633-2649962b3ef7 definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ideliveryoptimizationjob**](ideliveryoptimizationjob.md)
</dt> </dl>

 

