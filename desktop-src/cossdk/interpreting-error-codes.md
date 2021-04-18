---
description: Interpretieren von Fehler Codes
ms.assetid: df2fe03b-2f5f-4958-926f-17e3a025a9b5
title: Interpretieren von Fehler Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659ee7def9feff50d375a07ab201e1cca25bffd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343974"
---
# <a name="interpreting-error-codes"></a>Interpretieren von Fehler Codes

Nachdem Sie ermittelt haben, welche Anwendung die Ursache eines Problems ist, müssen Sie herausfinden, welcher Fehler aufgetreten ist. Abhängig von der Sprache, die von der Anwendung verwendet wird, werden Fehler ausgelöst und in unterschiedlichen Formaten gemeldet.

In Microsoft Visual C++ werden Erfolgs-, Warnungs-und Fehler Werte mithilfe einer 32-Bit-Zahl zurückgegeben, die als **HRESULT** bezeichnet wird. Eine Liste der System definierten **HRESULT** -Werte finden Sie in der Header Datei Winerror. h, die im Windows SDK enthalten ist. Diese Datei enthält alle com+-Fehlercodes und-Beschreibungen. Weitere Informationen zu **HRESULT** -Werten finden Sie unter [Fehlerbehandlung](/windows/desktop/com/error-handling-in-com).

In der Java-Sprache wird eine Instanz von com. ms. com. ComFailException ausgelöst, um einen Fehler anzugeben, bei dem das ComFailException-Objekt ein **HRESULT** angibt. Eine Instanz von com. ms. com. comerfolgreiches sexception gibt den Erfolg mit dem Rückgabewert false an. Weitere Informationen zum Interpretieren dieser Ausnahmen finden Sie in der Microsoft Visual J++-Dokumentation.

> [!Note]  
> Com+-Anwendungsserver Prozesse, die Visual J++-Objekte Hosting, werden nicht in den Leerlauf versetzt (selbst bei Null aktiven Objekten), es sei denn, Sie deaktivieren das JIT-Debugging in der VJ6-IDE. Weitere Informationen hierzu finden Sie in der Visual J++-Dokumentation.

 

In Visual Basic können Sie **HRESULT** -Werte abrufen, indem Sie die Err. Number-Eigenschaft untersuchen. Eine Beschreibung des Fehlers kann mit der Err. Description-Eigenschaft abgerufen werden.

Sie können auch das Dienstprogramm ERRLOOK in Microsoft Visual Studio verwenden, um eine System Fehlermeldung oder Modul Fehlermeldung abzurufen. ERRLOOK ruft den Fehlermeldungs Text automatisch ab, wenn Sie einen Hexadezimal-oder Dezimalwert aus dem Visual Studio-Debugger oder einer anderen Automatisierungs fähigen Anwendung ziehen und ablegen. Sie können auch einen Wert eingeben, indem Sie ihn entweder eingeben oder aus der IDE-Zwischenablage einfügen und auf die Option " **Suchen** " klicken.

Mit der folgenden C++-Methode wird eine Beschreibung des Fehlers basierend auf der Eingabe **HRESULT** ausgegeben.


```C++
#include <stdio.h>
#include <windows.h>
#include <tchar.h>

void ErrorDescription(HRESULT hr) 
{ 
     if(FACILITY_WINDOWS == HRESULT_FACILITY(hr)) 
         hr = HRESULT_CODE(hr); 
     TCHAR* szErrMsg; 

     if(FormatMessage( 
       FORMAT_MESSAGE_ALLOCATE_BUFFER|FORMAT_MESSAGE_FROM_SYSTEM, 
       NULL, hr, MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), 
       (LPTSTR)&szErrMsg, 0, NULL) != 0) 
     { 
         _tprintf(TEXT("%s"), szErrMsg); 
         LocalFree(szErrMsg); 
     } else 
         _tprintf( TEXT("[Could not find a description for error # %#x.]\n"), hr); 
}
```



In der folgenden Tabelle finden Sie Beschreibungen der allgemeinen Fehlercodes in com+.



| Fehlercodes                                                   | Definitionen                                                                                                                                                                                                      |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| COMAdmin \_ E \_ alinfo installiert<br/>                      | Das Objekt ist bereits registriert.<br/>                                                                                                                                                                     |
| App-Datei für COMAdmin- \_ E- \_ \_ Datei \_<br/>                   | Fehler beim Lesen der Anwendungsdatei.<br/>                                                                                                                                                          |
| COMAdmin \_ E \_ App- \_ Datei \_ Version<br/>                    | Ungültige Versionsnummer in der Anwendungsdatei.<br/>                                                                                                                                                           |
| COMAdmin \_ E \_ App- \_ Datei \_ Schreibfehler<br/>                  | Fehler beim Schreiben in die Anwendungsdatei.<br/>                                                                                                                                                       |
| COMAdmin \_ E \_ appdirnotfound<br/>                        | Das Installationsverzeichnis der Anwendung wurde nicht gefunden.<br/>                                                                                                                                                          |
| comqc \_ E- \_ Anwendung nicht in die \_ \_ Warteschlange eingereiht<br/>                 | Nur com+-Anwendungen, die als "Warteschlange" gekennzeichnet sind, können mit dem Moniker "Queue" erstellt werden.<br/>                                                                                                                      |
| "COMAdmin \_ E \_ Application" ist vorhanden.<br/>                     | Die Anwendung ist bereits installiert.<br/>                                                                                                                                                                 |
| "COMAdmin \_ E \_ ApplId" \_ entspricht der \_ CLSID.<br/>                | Eine CLSID mit der gleichen GUID wie die neue Anwendungs-ID ist bereits auf diesem Computer installiert.<br/>                                                                                                            |
| COMAdmin \_ E- \_ App wird \_ nicht \_ ausgeführt<br/>                     | Die angegebene Anwendung wird zurzeit nicht ausgeführt.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ AuthenticationLevel<br/>                   | Die erforderliche Authentifizierungs Ebene für die Aktualisierungs Anforderung kann nicht festgelegt werden.<br/>                                                                                                                                       |
| COMAdmin \_ E \_ badpath<br/>                               | Der Dateipfad ist ungültig.<br/>                                                                                                                                                                             |
| COMAdmin \_ E \_ badregistrylibid<br/>                      | Die ID der registrierten Typbibliothek ist ungültig.<br/>                                                                                                                                                            |
| COMAdmin \_ E \_ badregistryprogid<br/>                     | Die ProgID der Komponente fehlt oder ist beschädigt.<br/>                                                                                                                                                         |
| COMAdmin \_ E \_ kann \_ keinen \_ \_ App- \_ Proxy exportieren.<br/>          | Der Anwendungs Proxy kann nicht exportiert werden.<br/>                                                                                                                                                              |
| COMAdmin \_ E \_ kann \_ die \_ App nicht starten \_ .<br/>                  | Fehler beim Starten der Anwendung, da es sich entweder um eine Bibliotheks Anwendung oder einen Anwendungs Proxy handelt.<br/>                                                                                                       |
| COMAdmin \_ E \_ kann \_ die \_ \_ sys- \_ App nicht exportieren.<br/>            | Die Systemanwendung kann nicht exportiert werden.<br/>                                                                                                                                                             |
| COMAdmin \_ E \_ \_ \_ konnte die Komponente nicht abonnieren \_ .<br/>        | Der Benutzer kann diese Komponente nicht abonnieren, da die Komponente möglicherweise importiert wurde.<br/>                                                                                                             |
| "COMAdmin \_ E \_ cantcopyfile"<br/>                          | Beim Kopieren der Datei ist ein Fehler aufgetreten.<br/>                                                                                                                                                                   |
| COMAdmin \_ E \_ clsidoriidmismatch<br/>                    | Anwendungsdatei-CLSIDs oder IIDs stimmen nicht mit den entsprechenden DLLs überein.<br/>                                                                                                                                      |
| COMAdmin \_ E COMP-Vorgang ist \_ \_ \_ schlecht \_ dest<br/>                 | Fehler beim Verschieben der Komponente, da die Zielanwendung nicht mehr vorhanden ist.<br/>                                                                                                                       |
| COMAdmin \_ E \_ Comp- \_ Verschiebung \_ gesperrt<br/>                    | Das Verschieben der Komponente ist unzulässig, da die Quell-oder Zielanwendung entweder eine Systemanwendung ist oder zurzeit für Änderungen gesperrt ist.<br/>                                                |
| COMAdmin \_ E \_ compfile \_ badtlb<br/>                      | Die Typbibliothek konnte nicht geladen werden.<br/>                                                                                                                                                                 |
| COMAdmin \_ E \_ compfile \_ classnotavail<br/>               | Die DLL unterstützt die in der Typbibliothek aufgeführten Komponenten nicht.<br/>                                                                                                                                   |
| COMAdmin \_ E \_ compfile \_ doesnotexist<br/>                | Diese Datei ist nicht vorhanden.<br/>                                                                                                                                                                             |
| COMAdmin \_ E \_ compfile \_ getclassobj<br/>                 | Fehler bei der [**GetClassObject**](/windows/desktop/api/objidl/nf-objidl-iclassactivator-getclassobject) -Methode in der dll.<br/>                                                                                                                |
| COMAdmin \_ E \_ compfile \_ loaddllfail<br/>                 | Die dll konnte nicht geladen werden.<br/>                                                                                                                                                                          |
| COMAdmin \_ E \_ compfile \_ noregistrinar<br/>                 | Die in dieser Datei referenzierte Komponenten Registrierungsstelle ist nicht verfügbar.<br/>                                                                                                                                     |
| COMAdmin \_ E \_ compfile \_ notinstallable<br/>              | Die Datei enthält keine Komponenten oder Komponenten Informationen.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ coreqcompinstalliert<br/>                    | Eine Komponente in derselben dll ist bereits installiert.<br/>                                                                                                                                                     |
| COMAdmin \_ E \_ dllloadfailed<br/>                         | Die dll konnte nicht geladen werden.<br/>                                                                                                                                                                          |
| COMAdmin \_ E \_ DllRegisterServer<br/>                     | Die [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) -Funktion konnte nicht ausgeführt werden, als die Komponente installiert wurde.<br/>                                                                                                  |
| COMAdmin \_ E \_ EventClass \_ nicht \_ als \_ Abonnent<br/>      | Eine Ereignisklasse kann nicht als Abonnenten Komponente konfiguriert werden. Wenn versucht wird, ein Abonnement mit einer Ereignisklasse als Abonnent zu erstellen, wird dieser Fehler zurückgegeben.<br/>                          |
| COMAdmin \_ E \_ invaliduserids<br/>                        | Mindestens ein Benutzer in der Anwendungsdatei ist ungültig.<br/>                                                                                                                                              |
| COMAdmin \_ E \_ keymissing<br/>                            | Das Objekt wurde nicht im Katalog gefunden.<br/>                                                                                                                                                              |
| COMAdmin \_ E \_ lib- \_ App-Proxy nicht \_ \_ kompatibel<br/>         | Bibliotheksanwendungen und Anwendungs Proxys sind nicht kompatibel. Dieser Fehler wird zurückgegeben, wenn versucht wird, einen Anwendungs Proxy zu exportieren, und die Aktivierungs Eigenschaft der Anwendung eine Bibliothek ist. <br/> |
| COMAdmin \_ E \_ noregistryclsid<br/>                       | Die CLSID der Komponente fehlt oder ist beschädigt.<br/>                                                                                                                                                          |
| COMAdmin \_ E \_ noservershare<br/>                         | Es ist keine Server Dateifreigabe verfügbar.<br/>                                                                                                                                                                    |
| COMAdmin \_ E nicht \_ änderbar<br/>                         | Änderungen an diesem Objekt und seinen untergeordneten Objekten wurden deaktiviert.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ notdeleteable<br/>                         | Die Delete-Funktion wurde für dieses Objekt deaktiviert.<br/>                                                                                                                                                |
| COMAdmin \_ E \_ notinregistry<br/>                         | Das Objekt wurde in der Registrierung nicht gefunden.<br/>                                                                                                                                                                     |
| COMAdmin \_ E \_ nouser<br/>                                | Mindestens ein Benutzer ist ungültig.<br/>                                                                                                                                                                      |
| Das E-Objekt "COMAdmin" \_ \_ \_ ist \_ nicht \_ vorhanden.<br/>              | Eines der angegebenen-Objekte kann nicht gefunden werden.<br/>                                                                                                                                                         |
| das über \_ geordnete COMAdmin E- \_ Objekt \_ \_ fehlt.<br/>               | Eines der Objekte, das eingefügt oder aktualisiert wird, gehört nicht zu einer gültigen übergeordneten Auflistung.<br/>                                                                                                            |
| COMAdmin \_ E \_ ObjectErrors<br/>                          | Fehler beim Zugriff auf ein oder mehrere Objekte. Weitere Informationen finden Sie in der [**errorInfo**](errorinfo.md) -Auflistung.<br/>                                                                               |
| COMAdmin \_ E \_ objectexists<br/>                          | Das Objekt, das Sie hinzufügen oder umbenennen möchten, ist bereits vorhanden.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ objectinvalid<br/>                         | Mindestens eine der Eigenschaften des Objekts fehlt oder ist ungültig.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ objectnotpoolable<br/>                     | Dieses Objekt kann nicht in einem Pool zusammengefasst werden.<br/>                                                                                                                                                                      |
| COMAdmin \_ E \_ propertysavefailed<br/>                    | Mindestens eine Eigenschafts Einstellung ist entweder ungültig oder in Konflikt zueinander.<br/>                                                                                                                      |
| COMAdmin \_ E- \_ Eigenschafts \_ Überlauf<br/>                    | Der Eigenschafts Wert ist zu groß.<br/>                                                                                                                                                                      |
| COMAdmin \_ E \_ regfile \_ beschädigt<br/>                      | Die Registrierungsdatei ist beschädigt.<br/>                                                                                                                                                                     |
| COMAdmin \_ E \_ registertlb<br/>                           | Das System konnte die Typbibliothek nicht registrieren.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ registrarfailed<br/>                       | Fehler bei der Komponenten Registrierungsstelle.<br/>                                                                                                                                                     |
| COMAdmin \_ E \_ remoteinterface<br/>                       | Die Schnittstellen Informationen sind entweder nicht vorhanden oder wurden geändert.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ erfordert eine \_ andere \_ Plattform.<br/>         | Dieser Vorgang ist auf dieser Plattform nicht aktiviert.<br/>                                                                                                                                                       |
| die Rolle "COMAdmin \_ E" \_ \_ ist \_ nicht \_ vorhanden.<br/>                | Eine Rolle, die einer Komponente, Schnittstelle oder Methode zugewiesen ist, ist in der Anwendung nicht vorhanden.<br/>                                                                                                               |
| COMAdmin \_ E \_ roleexistiert<br/>                            | Die Rolle ist bereits vorhanden.<br/>                                                                                                                                                                              |
| COMAdmin \_ E \_ servicenotinstalliert<br/>                   | Der Dienst ist nicht installiert.<br/>                                                                                                                                                                         |
| COMAdmin \_ E- \_ Sitzung<br/>                               | Die Server Katalogversion wird nicht unterstützt.<br/>                                                                                                                                                          |
| COMAdmin- \_ e " \_ someallesypaused"<br/>                     | Mindestens ein angegebener Anwendungsprozess wurde bereits angehalten.<br/>                                                                                                                               |
| COMAdmin-e-Dateien \_ \_<br/>                    | Mindestens ein angegebener Anwendungsprozess wurde bereits ausgeführt.<br/>                                                                                                                              |
| COMAdmin \_ E- \_ Start- \_ App \_ benötigt \_ Komponenten<br/>         | Zum Starten der Anwendung müssen Sie über Komponenten in einer Anwendung verfügen.<br/>                                                                                                                                 |
| COMAdmin \_ E \_ svcapp \_ nicht in \_ Poolable \_ oder \_ recycelt<br/> | Die com+-Anwendungen, die als NT-Dienst ausgeführt werden, können nicht als in einem Pool zusammengefasst oder wieder verwendet werden.<br/>                                                                                                               |
| COMAdmin \_ E \_ systemapp<br/>                             | Dieser Vorgang kann für die Systemanwendung nicht ausgeführt werden.<br/>                                                                                                                                         |
| COMAdmin \_ E- \_ Benutzer \_ in \_ Gruppe<br/>                         | Mindestens ein Benutzer ist bereits einem lokalen Partitions Satz zugewiesen.<br/>                                                                                                                                      |
| COMAdmin \_ E \_ userpasswdnotvalid<br/>                    | Die in der Anwendung festgelegte Identität oder das Kennwort ist ungültig.<br/>                                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehler Isolation und FailFast-Richtlinie](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Ermitteln der Fehlerquelle](finding-the-source-of-an-error.md)
</dt> <dt>

[Ändern der Rückgabewerte durch com+](how-com--modifies-return-values.md)
</dt> <dt>

[Strategien für die Behandlung von Fehlern in com+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Problembehandlung](troubleshooting-the-com--crm.md)
</dt> </dl>

 

