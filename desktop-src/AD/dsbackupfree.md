---
title: Dsbackupfree-Funktion (ntdsbcli. h)
description: Gibt Arbeitsspeicher frei, der durch die Active Directory Domain Services Sicherungs-und Wiederherstellungs Funktionen zugeordnet
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Dsbackupfree-Funktions Active Directory
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27855eeb3417eede371357528457248857c3e626
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858832"
---
# <a name="dsbackupfree-function"></a>Dsbackupfree-Funktion

\[Diese Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie ab Windows Vista [Volumeschattenkopie-Dienst (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

Die **dsbackupfree** -Funktion gibt Arbeitsspeicher frei, der durch die Active Directory Domain Services Sicherungs-und Wiederherstellungs Funktionen belegt wird Die folgenden Funktionen weisen Arbeitsspeicher zu, der mit der **dsbackupfree** -Funktion freigegeben werden muss.

-   [**Dsbackupgetbackuplogs**](dsbackupgetbackuplogs.md)
-   [**Dsbackupgetdatabasenames**](dsbackupgetdatabasenames.md)
-   [**Dsbackupprepare**](dsbackupprepare.md)
-   [**Dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a>Syntax


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvbuffer* \[ in\]
</dt> <dd>

Ein Zeiger auf den Speicherpuffer, der freigegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Dsbackupgetbackuplogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**Dsbackupgetdatabasenames**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**Dsbackupprepare**](dsbackupprepare.md)
</dt> <dt>

[**Dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[Sichern eines Active Directory Servers](backing-up-an-active-directory-server.md)
</dt> <dt>

[Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)
</dt> </dl>

 

