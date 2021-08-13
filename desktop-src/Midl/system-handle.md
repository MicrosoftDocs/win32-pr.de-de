---
title: system_handle-Attribut
description: Das \system_handle\-Attribut gibt einen systemdefinierte Handletyp an.
keywords:
- system_handle-Attribut MIDL
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1cc89818db201f1aca84aa63c6aa49b6b7d9f80b7b6c5e211e724004606c653e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641266"
---
# <a name="system_handle-attribute"></a>system_handle-Attribut

Das \[  \] system_handle-Attribut gibt einen systemdefinierte Handletyp an, der den Zugriff auf ein Systemobjekt darstellt.

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*system-handle-type* 
</dt> <dd>

Gibt eine der Systemhandletypoptionen an.

Die gültigen Optionen sind:
* [sh_composition](sh-composition.md) : Ein DirectComposition-Oberflächenhandle
* [sh_event:](sh-event.md) Ein benanntes oder unbenanntes Ereignisobjekt
* [sh_file:](sh-file.md) Eine Datei oder ein E/A-Gerät
* [sh_job:](sh-job.md) Ein Auftragsobjekt
* [sh_mutex:](sh-mutex.md) Ein benanntes oder unbenanntes Mutexobjekt
* [sh_pipe:](sh-pipe.md) Ein anonymes oder benanntes Pipeobjekt
* [sh_process:](sh-process.md) Ein Prozessobjekt
* [sh_reg_key:](sh-reg-key.md) Ein Registrierungsschlüssel
* [sh_section:](sh-section.md) Abschnitt "Freigegebener Arbeitsspeicher"
* [sh_semaphore:](sh-semaphore.md) Ein benanntes oder unbenanntes Semaphorobjekt
* [sh_socket:](sh-socket.md) Ein WinSock-Socketobjekt
* [sh_thread:](sh-thread.md) Ein Threadobjekt
* [sh_token:](sh-token.md) Ein Zugriffstokenobjekt

</dd> <dt>

*optional-access-mask*
</dt> <dd>

Fordert optional bestimmte Zugriffsrechte an, die auf das duplizierte Handle angewendet werden. Wenn dies nicht angegeben ist, wird das Handle standardmäßig mit dem gleichen Zugriff dupliziert. 

Um eine andere Zugriffsebene anzugeben, verwenden Sie objektspezifische Zugriffsrechte, die dem ausgewählten zugrunde liegenden Systemobjekt entsprechen.

Weitere Informationen zur Weitergabe von Zugriffsrechten während der Duplizierung finden Sie in der [DuplicateHandle-Dokumentation.](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

Links zu Listen mit Zugriffsrechten für jeden Objekttyp finden Sie in der *DuplicateHandle-Referenz* sowie in den Überschriften **siehe auch** auf jeder `sh_*` Parameterseite.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um dieses Attribut verwenden zu können, muss das `-target` Flag `NT100` auf (oder höher) festgelegt werden, wenn midl.exe ausgeführt wird.

Systemhandles sind Handles, die vom Betriebssystem definiert werden, um Zugriff auf eine Systemressource zu ermöglichen. Der spezifische Typ des Objekts hinter dem Handle muss beim Deklarieren des Attributs angegeben werden.

Bei einem mit markierten Handle `[in]` wird das Handle in die Remoteprozedur dupliziert und bleibt für die Dauer dieser Prozedur gültig. Bei Rückgabe aus der Remoteprozedur wird das duplizierte Handle freigegeben. Um den Zugriff auf das zugrunde liegende Objekt beizubehalten, muss die Remoteanwendung das Handle in ihren eigenen Adressraum duplizieren.

Im Gegensatz dazu verliert die Remoteprozedur den Besitz für ein handle, das als markiert `[out]` ist, wenn eine Remoteprozedur ein Handle von einem Aufruf zurückgibt. Um den Zugriff auf das zugrunde liegende Objekt beizubehalten, sollte die Remoteprozedur das Handle duplizieren und das Duplikat zurückgeben. Das zurückgegebene Handle gehört dann dem Aufrufer, der die Verantwortung übernimmt, es zu schließen, wenn der Zugriff auf das zugrunde liegende Systemobjekt nicht mehr erforderlich ist.

Da dies ein Mechanismus zum Weiterleiten des Zugriffs auf ein Systemobjekt ist, gilt dieses Attribut nur für Aufrufe zwischen Prozeduren auf demselben Computer.

Die Erstellungs- und Zugriffsparameter, die dem zugrunde liegenden Objekt hinter dem Systemhandle bei der Erstellung übergeben werden, bestimmen, ob es erfolgreich in den Remoteprozedurkontext gemarshallt werden kann.

Ein Array von `system_handle` kann entweder in oder ausgehend mit der Syntax übergeben werden, die in der Dokumentation [**size_is Attributs**](size-is.md) enthalten ist.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen werden mehrere Verwendungen von `system_handle` verwendet. Ein vollständiges Beispiel finden Sie im [SystemHandlePassing-Beispiel.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)

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

## <a name="see-also"></a>Weitere Informationen:

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

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[Sicherheitsbeschreibungen](../secauthz/security-descriptors.md)
</dt></dl>
