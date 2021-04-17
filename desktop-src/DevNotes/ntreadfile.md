---
description: Liest Daten aus einer geöffneten Datei.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Ntreadfile-Funktion (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523176"
---
# <a name="ntreadfile-function"></a>Ntreadfile-Funktion

Liest Daten aus einer geöffneten Datei.

Diese Funktion ist der Benutzermodus, der der im Windows-Treiberkit (WDK) dokumentierten [**zwlesefile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) -Funktion entspricht.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FILEHANDLE* \[ in\]
</dt> <dd>

Handle für das Datei Objekt. Dieses Handle wird durch einen erfolgreichen Aufrufen von [**ntkreatefile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) oder [**ntopenfile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile)erstellt.

</dd> <dt>

*Ereignis* \[ in, optional\]
</dt> <dd>

Ein Handle für ein Ereignis Objekt, das auf den signalisierten Zustand festgelegt werden soll, nachdem der Lesevorgang abgeschlossen wurde. Für Geräte-und zwischen Treiber sollte dieser Parameter auf **null** festgelegt werden.

</dd> <dt>

*Apcroutine* \[ in, optional\]
</dt> <dd>

Dieser Parameter ist reserviert. Für Geräte-und zwischen Treiber sollte dieser Zeiger auf **null** festgelegt werden.

</dd> <dt>

*Apccontext* \[ in, optional\]
</dt> <dd>

Dieser Parameter ist reserviert. Für Geräte-und zwischen Treiber sollte dieser Zeiger auf **null** festgelegt werden.

</dd> <dt>

*Iostatus Block* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [**IO- \_ Status \_ Block**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) Struktur, die den endgültigen Abschluss Status und Informationen zum angeforderten Lesevorgang empfängt. Der **informationsmember** erhält die Anzahl der tatsächlich aus der Datei gelesenen Bytes.

</dd> <dt>

*Puffer* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen vom Aufrufer zugewiesenen Puffer, der die aus der Datei gelesenen Daten empfängt.

</dd> <dt>

*Länge* \[ in\]
</dt> <dd>

Die Größe des Puffers in Byte, auf den durch den *Puffer* gezeigt wird.

</dd> <dt>

*Byteoffset* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den Start Byte Offset in der Datei angibt, in der der Lesevorgang beginnt. Wenn versucht wird, über das Dateiende hinaus zu lesen, gibt **ntreadfile** einen Fehler zurück.

Wenn für den Aufrufen von [**ntkreatefile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) *eine der Dateien für die* synchrone e/a-Benachrichtigung oder eine synchrone e/a-Datei für e/a-Vorgänge festgelegt \_ \_ \_ \_ \_ \_ ist, behält der e/a-Manager die aktuelle Datei Wenn dies der Fall ist, kann der Aufrufer von **ntreadfile** angeben, dass der aktuelle Offset der Dateiposition anstelle eines expliziten *Byteoffset* -Werts verwendet werden soll. Diese Angabe kann mithilfe einer der folgenden Methoden erfolgen:

-   Geben Sie einen Zeiger auf einen **großen \_ ganzzahligen** Wert an, bei dem das **highpart** -Element auf-1 festgelegt ist und das **LowPart** -Element, das auf die System definierte Wert Datei festgelegt ist, \_ \_ Datei \_ Zeiger \_

-   Übergeben Sie einen **null** -Zeiger für *Byteoffset*.

**Ntreadfile** aktualisiert die aktuelle Dateiposition durch Hinzufügen der Anzahl der gelesenen Bytes, wenn der Lesevorgang abgeschlossen wird, wenn die aktuelle Dateiposition verwendet wird, die vom e/a-Manager verwaltet wird.

Auch wenn der e/a-Manager die aktuelle Dateiposition beibehält, kann der Aufrufer diese Position zurücksetzen, indem er einen expliziten *Byteoffset* -Wert an **ntreadfile** übergibt. Dadurch wird die aktuelle Dateiposition automatisch in diesen *Byteoffset* -Wert geändert, der Lesevorgang ausgeführt und die Position entsprechend der Anzahl der tatsächlich gelesenen Bytes aktualisiert. Diese Technik bietet dem Aufrufer den atomarischen Seek-und Lesedienst.

</dd> <dt>

*Schlüssel* \[ in, optional\]
</dt> <dd>

Für Geräte-und zwischen Treiber sollte dieser Zeiger auf **null** festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Ntreadfile** gibt entweder \_ den Status Erfolg oder den entsprechenden NTSTATUS-Fehlercode zurück.

## <a name="remarks"></a>Bemerkungen

Aufrufer von **ntreadfile** müssen bereits [**ntkreatefile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) mit der Datei \_ Read \_ Data oder dem \_ Wert für einen generischen Lesevorgang im *desiredAccess* -Parameter aufgerufen haben.

Wenn der vorherige Befehl von [**ntkreatefile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) das Flag " \_ keine \_ zwischen \_ Pufferung für Datei" im Parameter " *kreateoptions* " auf " **ntkreatefile**" festgelegt hat, müssen die Parameter " *length* " und " *Byteoffset* " in " **ntreadfile** " Vielfachen der Sektorgröße sein Weitere Informationen finden Sie unter **ntkreatefile**.

**Ntreadfile** beginnt mit dem Lesen aus dem angegebenen *Byteoffset* oder der aktuellen Dateiposition in den angegebenen *Puffer*. Der Lesevorgang wird unter einer der folgenden Bedingungen beendet:

-   Der Puffer ist voll, weil die vom *length* -Parameter angegebene Anzahl von Bytes gelesen wurde. Daher können keine weiteren Daten ohne Überlauf in den Puffer eingefügt werden.

-   Das Dateiende wird während des Lesevorgangs erreicht, sodass keine weiteren Daten in der Datei vorhanden sind, die in den Puffer übertragen werden.

Wenn der Aufrufer die Datei mit dem in *desiredAccess* festgelegten synchronisierungsflag geöffnet hat, kann der aufrufende Thread mit dem Abschluss des Lesevorgangs synchronisiert werden, indem auf das Datei Handle, *FILEHANDLE*, gewartet wird. Das Handle wird jedes Mal signalisiert, wenn ein e/a-Vorgang, der für das Handle ausgegeben wurde, abgeschlossen ist. Der Aufrufer darf jedoch nicht auf ein Handle warten, das für den synchronen Dateizugriff geöffnet wurde (Datei synchrone e/a-Warnung oder synchrone e/a- \_ \_ \_ \_ \_ \_ Warnung). In diesem Fall wartet **ntreadfile** im Auftrag des Aufrufers und gibt erst dann zurück, wenn der Lesevorgang beendet wurde. Der Aufrufer kann auf das Datei Handle nur dann sicher warten, wenn alle drei der folgenden Bedingungen erfüllt sind:

-   Das Handle wurde für den asynchronen Zugriff geöffnet (d. h., es wurde kein synchrones e/a- \_ Flag " \_ \_ *xxx* " angegeben)

-   Das Handle wird nur für einen e/a-Vorgang gleichzeitig verwendet.

-   **Ntreadfile** hat Status \_ Ausstehend zurückgegeben.

Ein Treiber sollte **ntreadfile** im Kontext des System Prozesses abrufen, wenn eine der folgenden Bedingungen zutrifft:

-   Der Treiber hat das Datei Handle erstellt, das an **ntreadfile** weitergeleitet wird.

-   **Ntreadfile** benachrichtigt den Treiber über den e/a-Abschluss mithilfe eines Ereignisses, das der Treiber erstellt hat.

-   **Ntreadfile** benachrichtigt den Treiber über den e/a-Abschluss mithilfe einer APC-Rückruf Routine, die der Treiber an **ntreadfile** übergibt.

Datei-und Ereignis Handles sind nur im Prozess Kontext gültig, in dem die Handles erstellt werden. Um Sicherheitslücken zu vermeiden, sollte der Treiber daher jedes beliebige Datei-oder Ereignis handle, das er im Kontext des System Prozesses an **ntreadfile** übergibt, und nicht den Kontext des Prozesses, in dem sich der Treiber befindet, erstellen.

Ebenso sollte **ntreadfile** im Kontext des System Prozesses aufgerufen werden, wenn der Treiber über einen e/a-Abschluss mithilfe eines APC benachrichtigt wird, da APCs immer im Kontext des Threads ausgelöst werden, der die e/a-Anforderung ausgibt. Wenn der Treiber **ntreadfile** im Kontext eines anderen Prozesses als dem System aufruft, kann das APC unbegrenzt verzögert oder überhaupt nicht ausgelöst werden.

Weitere Informationen zum Arbeiten mit Dateien finden Sie unter [Verwenden von Dateien in einem Treiber](/windows-hardware/drivers/kernel/using-files-in-a-driver).

Aufrufer von **ntreadfile** müssen auf der Ebene "iriql = passiv" \_ und [mit aktivierten speziellen Kernel-APCs](/windows-hardware/drivers/kernel/disabling-apcs)ausgeführt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                    |
| Zielplattform<br/>          | <dl> <dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>WDM. h (Include WDM. h, ntddk. h oder ntifs. h)</dt> </dl>                   |
| Bibliothek<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll (Benutzermodus)</dt> </dl>                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Keinitializeevent**](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[**Ntqueryinformationfile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[**Ntsetinformationfile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[**Ntwrite-Datei**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 
