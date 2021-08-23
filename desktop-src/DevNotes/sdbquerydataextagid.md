---
description: Ruft Daten aus den angegebenen Einträgen ab, die zu einem EXE-Eintrag gehören.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: SdbQueryDataExTagID-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 19477385fb70f65c560d1a13d479fc4c2ce1853220aff6ac32a75f3634a40d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815380"
---
# <a name="sdbquerydataextagid-function"></a>SdbQueryDataExTagID-Funktion

Ruft Daten aus den angegebenen Einträgen ab, die zu einem EXE-Eintrag gehören.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdb* \[ In\]
</dt> <dd>

Ein Handle für die Shim-Datenbank.

</dd> <dt>

*tiExe* \[ In\]
</dt> <dd>

Die [**TAGID**](tagid.md) des EXE-Eintrags.

</dd> <dt>

*lpszDataName* \[ in, optional\]
</dt> <dd>

Der Name des abzurufenden Dateneintrags. Um mehrere Einträge anzugeben, trennen Sie die Namen durch den schrägen Schrägstrich (" \\ "). Wenn dieser Parameter **NULL ist,** versucht die Funktion, alle Dateneinträge zurückgibt.

</dd> <dt>

*lpdwDataType* \[ out, optional\]
</dt> <dd>

Der Datentyp der zurückgegebenen Einträge. Dieser Parameter kann einen der folgenden Werte haben:

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

**REG \_ BINARY**
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

**REG \_ DWORD**
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

**REG \_ MULTI \_ SZ**
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

**REG \_ NONE**
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

**REG \_ QWORD**
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

**REG \_ SZ**
</dt> </dl> </dd> <dt>

*lpBuffer* \[ out\]
</dt> <dd>

Der Puffer, der die Daten empfängt. Wenn der Puffer nicht groß genug ist, um die Daten zu enthalten, schlägt die Funktion fehl und gibt **ERROR \_ INSUFFICIENT BUFFER \_ zurück.**

</dd> <dt>

*lpcbBufferSize* \[ in, out, optional\]
</dt> <dd>

Die Größe des *lpBuffer-Puffers* in Bytes.

</dd> <dt>

*ptiData* \[ out\]
</dt> <dd>

Die [**TAGID**](tagid.md) des Dateneintrags.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                                    | Beschreibung                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>       | Mindestens ein Eingabeparameter ist falsch.<br/>                  |
| <dl> <dt>**FEHLER: \_ INTERNE \_ \_ DATENBANKBESCHÄDIGUNG**</dt> </dl> | Für den EXE-Eintrag wurden keine Dateneinträge gefunden.<br/>               |
| <dl> <dt>**FEHLER: \_ NICHT GENÜGEND \_ PUFFER**</dt> </dl>     | Der Puffer ist nicht groß genug, um die Dateneinträge zu enthalten.<br/> |
| <dl> <dt>**FEHLER: \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>      | Fehler bei der Speicherzuweisung.<br/>                               |
| <dl> <dt>**FEHLER \_ NICHT \_ GEFUNDEN**</dt> </dl>               | Ein Dateneintrag mit dem Namen *lpszDataName* wurde nicht gefunden.<br/>    |
| <dl> <dt>**FEHLER \_ ERFOLGREICH**</dt> </dl>                  | Die Funktion wurde erfolgreich abgeschlossen.<br/>                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




