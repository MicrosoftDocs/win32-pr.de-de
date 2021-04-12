---
description: Ruft Daten aus den angegebenen Einträgen ab, die zu einem exe-Eintrag gehören.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: Sdbquerydataextagid-Funktion
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
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392938"
---
# <a name="sdbquerydataextagid-function"></a>Sdbquerydataextagid-Funktion

Ruft Daten aus den angegebenen Einträgen ab, die zu einem exe-Eintrag gehören.

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

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*tiexe* \[ in\]
</dt> <dd>

Die [**TagID**](tagid.md) des exe-Eintrags.

</dd> <dt>

*lpszdataname* \[ in, optional\]
</dt> <dd>

Der Name des Daten Eintrags, der abgerufen werden soll. Wenn Sie mehrere Einträge angeben möchten, trennen Sie die Namen durch den umgekehrten Schrägstrich (" \\ "). Wenn dieser Parameter **null** ist, versucht die Funktion, alle Dateneinträge zurückzugeben.

</dd> <dt>

*lpdwdatatype* \[ Out, optional\]
</dt> <dd>

Der Datentyp der zurückgegebenen Einträge. Dieser Parameter kann einen der folgenden Werte aufweisen:

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

**REG- \_ Binärdatei**
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

**REG \_ DWORD**
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

**REG \_ \_ MultiSZ**
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

**REG \_ None**
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

**REG \_ QWORD**
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

**REG- \_ SZ**
</dt> </dl> </dd> <dt>

*lpBuffer* \[ vorgenommen\]
</dt> <dd>

Der Puffer, der die Daten empfängt. Wenn der Puffer nicht groß genug ist, um die Daten zu enthalten, schlägt die Funktion fehl und gibt einen **fehlerhaften \_ \_ Puffer** zurück.

</dd> <dt>

*lpcbbuffersize* \[ in, out, optional\]
</dt> <dd>

Die Größe des *lpBuffer* -Puffers in Bytes.

</dd> <dt>

*ptidata* \[ vorgenommen\]
</dt> <dd>

Die [**TagID**](tagid.md) des Daten Eintrags.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                                    | Beschreibung                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>       | Mindestens ein Eingabeparameter ist falsch.<br/>                  |
| <dl> <dt>**Fehler bei \_ interner \_ DB- \_ Datenbank.**</dt> </dl> | Es wurden keine Dateneinträge für den exe-Eintrag gefunden.<br/>               |
| <dl> <dt>**Fehler \_ beim \_ Puffer.**</dt> </dl>     | Der Puffer ist nicht groß genug, um die Dateneinträge zu enthalten.<br/> |
| <dl> <dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt> </dl>      | Die Speicher Belegung ist fehlgeschlagen.<br/>                               |
| <dl> <dt>**Fehler \_ nicht \_ gefunden.**</dt> </dl>               | Ein Dateneintrag mit dem Namen *lpszdataname* wurde nicht gefunden.<br/>    |
| <dl> <dt>**Fehler \_ erfolgreich**</dt> </dl>                  | Die Funktion wurde erfolgreich abgeschlossen.<br/>                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




