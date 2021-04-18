---
title: system_handle-Attribut
description: Das Attribut \ system_handle \ gibt einen System definierten Handlertyp an.
keywords:
- system_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f414654cdbd2eb07837455174f6142005f56a4b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106371832"
---
# <a name="system_handle-attribute"></a>system_handle-Attribut

Das \[ **system_handle** - \] Attribut gibt einen System definierten Handlertyp an, der den Zugriff auf ein Systemobjekt darstellt.

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*System Handle-Typ* 
</dt> <dd>

Gibt eine der Optionen für den systembehandlertyp an.

Die gültigen Optionen sind:
* [sh_composition](sh-composition.md) : ein directcomposition-Oberflächen handle
* [sh_event](sh-event.md) ein benanntes oder unbenanntes Ereignis Objekt
* [sh_file](sh-file.md) : eine Datei oder ein e/a-Gerät
* [sh_job](sh-job.md) : ein Auftrags Objekt
* [sh_mutex](sh-mutex.md) ein benanntes oder unbenanntes Mutex-Objekt
* [sh_pipe](sh-pipe.md) -ein anonymes oder Named Pipe-Objekt
* [sh_process](sh-process.md) -ein Prozess Objekt
* [sh_reg_key](sh-reg-key.md) -Registrierungsschlüssel
* [sh_section](sh-section.md) -A Shared Memory-Abschnitt
* [sh_semaphore](sh-semaphore.md) ein benanntes oder unbenanntes Semaphor-Objekt
* [sh_socket](sh-socket.md) -ein Winsock-Socketobjekt
* [sh_thread](sh-thread.md) : ein Thread Objekt
* [sh_token](sh-token.md) : ein zugriffstokenobjekt.

</dd> <dt>

*optional-Access-Mask*
</dt> <dd>

Fordert optional bestimmte Zugriffsrechte an, die auf das duplizierte handle angewendet werden. Wenn dies nicht angegeben ist, wird das Handle standardmäßig mit demselben Zugriff dupliziert. 

Um eine andere Zugriffsebene anzugeben, verwenden Sie objektspezifische Zugriffsrechte, die dem zugrunde liegenden Systemobjekt entsprechen.

Weitere Informationen zur Weitergabe von Zugriffsrechten während der Duplizierung finden Sie in der [duplikatandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Dokumentation.

Links zu Listen mit Zugriffsrechten für jeden Objekttyp finden Sie sowohl in der *dupliktandle* -Referenz als auch in den " **Siehe auch** "-Überschriften der einzelnen `sh_*` Parameter Seiten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut zu verwenden, muss das- `-target` Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.

System Handles sind Handles, die vom Betriebssystem definiert werden, um den Zugriff auf eine System Ressource bereitzustellen. Der spezifische Typ des Objekts hinter dem Handle muss beim Deklarieren des Attributs angegeben werden.

Bei einem markierten Handle `[in]` wird das Handle in die Remote Prozedur dupliziert und bleibt für die Dauer der Prozedur gültig. Bei der Rückgabe von der Remote Prozedur wird das doppelte Handle freigegeben. Um den Zugriff auf das zugrunde liegende Objekt aufrechtzuerhalten, muss die Remote Anwendung das Handle in seinen eigenen Adressraum duplizieren.

Im Gegensatz dazu geht bei einem markierten Handle `[out]` , wenn eine Remote Prozedur ein Handle von einem-Befehl zurückgibt, der Besitz der Remote Prozedur verloren. Um den Zugriff auf das zugrunde liegende Objekt aufrechtzuerhalten, sollte die Remote Prozedur das Handle duplizieren und das Duplikat zurückgeben. Der zurückgegebene Handle wird dann im Besitz des Aufrufers, der die Verantwortung dafür übernimmt, ihn zu schließen, wenn der Zugriff auf das zugrunde liegende Systemobjekt nicht mehr erforderlich ist.

Da dies ein Mechanismus zum Weiterleiten des Zugriffs auf ein Systemobjekt ist, gilt dieses Attribut nur für Aufrufe zwischen Prozeduren auf dem gleichen Computer.

Die Erstellungs-und Zugriffsparameter, die dem zugrunde liegenden Objekt hinter dem System Handle bei der Erstellung erteilt werden, legen vor, ob es erfolgreich in den Remote Prozedur Kontext gemarshallt werden kann.

Ein Array von `system_handle` kann mit der Syntax, die in der [**size_is-Attribut**](size-is.md) Dokumentation gefunden wird, entweder ein-oder ausgehend werden.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen werden verschiedene Verwendungen von verwendet `system_handle` . Ein umfassendes Beispiel finden Sie im [System Lenker](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) -Beispiel.

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 10 Anniversary Update (Version 1607, Build 14393) |
| Unterstützte Mindestversion (Server) | Windows Server 2016 (Build 14393) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[/target-Schalter](./-target.md)
</dt> <dt>

[Bindung und Handles](../Rpc/binding-and-handles.md)
</dt> <dt>

[Handles und Objekte](../sysinfo/handles-and-objects.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Duplialisiehandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[Sicherheitsbeschreibungen](../secauthz/security-descriptors.md)
</dt></dl>
