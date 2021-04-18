---
description: Sie können die WMI-Component Object Model (com)-API verwenden, um Verwaltungs Client Anwendungen zu schreiben oder einen neuen WMI-Anbieter zu erstellen.
ms.assetid: 5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1
ms.tgt_platform: multiple
title: COM-API für WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb585badeeeaae947906bbfc783baf355863e05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347505"
---
# <a name="com-api-for-wmi"></a>COM-API für WMI

Sie können die WMI-Component Object Model (com)-API verwenden, um Verwaltungs Client Anwendungen zu schreiben oder einen neuen WMI- [*Anbieter*](gloss-p.md)zu erstellen. Die com-API-Referenz enthält Informationen für erweiterte Systemadministratoren sowie für Entwickler, die Client-und Anbieter Anwendungen schreiben.

Weitere Informationen zum Schreiben von WMI Enterprise Management-Anwendungen finden [Sie unter Erstellen einer WMI-Anwendung mithilfe von C++](creating-a-wmi-application-using-c-.md). Weitere Informationen zum Schreiben eines WMI-Anbieters finden [Sie unter Bereitstellen von Daten für WMI](providing-data-to-wmi.md).

> [!Note]  
> WMI unterstützt nur die C++-Entwicklung mithilfe der Entwicklungssysteme Microsoft Visual C++ Version 6,0 und höher. Sie können jedoch auch andere Compiler (z. b. die von Borland und Watcom) verwenden.

 

Jedes der verschiedenen WMI-Objekte erbt von einer Schnittstelle, die letztendlich von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle geerbt wurde. COM bestimmt, wie objektimplementierer oder Schnittstellen Aufgaben wie die Speicherverwaltung, die Parameter Verwaltung und das Multithreading verarbeiten. Durch die Konformität mit com stellt die com-API für WMI sicher, dass Sie die Funktionalität unterstützt, die von den Schnittstellen jedes WMI-Objekts bereitgestellt wird.

Der Zugriff auf WMI erfolgt über die folgenden WMI-spezifischen COM-Schnittstellen.



| Schnittstelle                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)                         | Enumerator, der mit Objekten des Typs [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)funktioniert. Sie ähnelt Standard-com-Enumeratoren, wie z. b. [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).                                                                                                      |
| [**Imuf Compiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)                                         | Diese Schnittstelle wird von Mofd.dll implementiert und stellt eine COM-Schnittstelle bereit, die vom MOF-Compiler und anderen Anwendungen, die MOF-Dateien kompilieren, verwendet wird.                                                                                                                                                       |
| [**Iunsecuredapartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)                           | Wird verwendet, um den Prozess der asynchronen Aufrufe von einem Client Prozess zu vereinfachen.                                                                                                                                                                                                                           |
| [**Iwbembackuprestore**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbembackuprestore)                             | Sichert und stellt den Inhalt des WMI-Repository wieder her.                                                                                                                                                                                                                                                  |
| [**Iwbemcallresult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)                                   | Wird für [semisynchrone](making-a-semisynchronous-call-with-c--.md) Aufrufe der [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle verwendet. Wenn solche Aufrufe durchführen, wird die aufgerufene **IWbemServices** -Methode sofort zusammen mit einem [**iwbemcallresult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) -Objekt zurückgegeben.                    |
| [**Iwbemkausalityanalysis**](iwbemcausalityaccess.md)                       | Verfolgt die untergeordneten Anforderungen, die von einer übergeordneten Anforderung generiert werden.                                                                                                                                                                                                                                            |
| [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)                                 | Enthält und manipuliert sowohl Klassendefinitionen als auch Klassenobjekt Instanzen. Entwickler müssen diese Schnittstelle nicht implementieren. WMI stellt seine Implementierung bereit.                                                                                                                                                 |
| [**Iwbemconfigurerefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher)                   | Wird vom Client Code zum Hinzufügen oder Entfernen von Enumeratoren, Objekten und eingefügten freshern zu einem Aktualisierungs Programm verwendet.                                                                                                                                                                                                         |
| [**"IWbemContext"**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)                                         | Wird optional verwendet, um den Anbietern beim Übermitteln von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Aufrufen an die Windows-Verwaltung zusätzliche Kontextinformationen mitzuteilen.                                                                                                                                             |
| [**Iwbementkopppledbasiceventprovider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider) | Registriert entkoppelte Anbieter bei WMI.                                                                                                                                                                                                                                                                    |
| [**Iwbementkopppledregistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar)                   | Verknüpft entkoppelte Anbieter mit WMI. Mit dieser Schnittstelle kann ein vom Prozess gehosteter Anbieter die Interoperabilitäts Lebensdauer der Schnittstelle definieren und mit anderen Anbietern koexistieren.                                                                                                                        |
| [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider)             | Stellt die primäre Schnittstelle für einen Ereignisconsumeranbieter bereit. Über diese Schnittstelle und die [**FindConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventconsumerprovider-findconsumer) -Methode kann ein Ereignisconsumeranbieter angeben, welche Ereignisconsumer ein bestimmtes Ereignis erhalten sollen.                                          |
| [**Iwbemeventprovider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider)                             | Wird verwendet, um die Kommunikation mit einem Ereignis Anbieter zu initiieren.                                                                                                                                                                                                                                                     |
| [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)           | Optional von Ereignis Anbietern implementiert, die wissen möchten, welche Arten von Ereignis Abfrage filtern derzeit aktiv sind, um die Leistung zu optimieren.                                                                                                                                                                 |
| [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity)             | Optional von Ereignis Anbietern implementiert, die den Zugriff des Consumers auf Ihre Ereignisse einschränken möchten.                                                                                                                                                                                                             |
| [**Iwbemeventsink**](iwbemeventsink.md)                                     | Initiiert die Kommunikation mit einem Ereignis Anbieter unter Verwendung eines eingeschränkten Satzes von Abfragen. Diese Schnittstelle erweitert [**iwbebobjectsink**](iwbemobjectsink.md)und bietet neue Methoden für Sicherheit und Leistung.                                                                                          |
| [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider)                           | Ermöglicht Anbietern das Bereitstellen von aktualisierbaren Objekten und Enumeratoren.                                                                                                                                                                                                                                           |
| [**Iwbemhiperfaufumum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum)                                   | Wird in Aktualisierungs Vorgängen verwendet, um schnellen Zugriff auf Enumerationen von Instanzobjekten zu ermöglichen.                                                                                                                                                                                                                  |
| [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)                                         | Ruft den anfänglichen Namespace Zeiger auf die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle für WMI auf einem bestimmten Host Computer ab.                                                                                                                                                                         |
| [**Iwbemubjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)                               | Bietet Zugriff auf die Methoden und Eigenschaften eines Objekts. Ein [**iwbefubjectaccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) -Objekt ist ein Container für eine Instanz, die [*von einem*](gloss-r.md)Aktualisierungs Programm aktualisiert wurde.                                                                                           |
| [**Iwbemubjectsink**](iwbemobjectsink.md)                                   | Wird zum Empfangen der Ergebnisse von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) und bestimmter Ereignis Benachrichtigungs Typen verwendet.                                                                                                                                                                                       |
| [**Iwbemubjecttextrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)                             | Wird verwendet, um [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Instanzen in und aus unterschiedlichen Textformaten zu übersetzen.                                                                                                                                                                                               |
| [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)                       | Unterstützt das Abrufen und Aktualisieren einzelner Eigenschaften in einer Instanz einer WMI-Klasse.                                                                                                                                                                                                                      |
| [**Iwbemprovideridentity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemprovideridentity)                       | Wird von einem Ereignis Anbieter implementiert, wenn sich der Anbieter unter Verwendung von mehr als einem **Namen** (mehrere Instanzen von [**\_ \_ Win32Provider**](--win32provider.md)) mit demselben [CLSID](../com/clsid.md) -Wert registriert. Die-Klasse stellt einen Mechanismus bereit, um zu unterscheiden, welcher benannte Anbieter verwendet werden soll. |
| [**Iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)                               | Wird zum Initialisieren von Anbietern verwendet.                                                                                                                                                                                                                                                                              |
| [**Iwbemproviderinitsink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink)                       | Wird von WMI implementiert und von Anbietern aufgerufen, um den Initialisierungs Status zu melden.                                                                                                                                                                                                                                |
| [**Iwbemqualifierset**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset)                               | Fungiert als Container für den gesamten Satz von benannten Qualifizierern für eine einzelne Eigenschaft oder ein gesamtes Objekt (eine Klasse oder eine Instanz).                                                                                                                                                                                   |
| [**IWbemQuery**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbemquery)                                             | Stellt einen Einstiegspunkt bereit, über den eine [*WMI Query Language*](gloss-w.md) (WQL)-Abfrage analysiert werden kann.                                                                                                                                                                        |
| [**Iwbemfreshsher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)                                     | Bietet einen Einstiegspunkt, über den aktualisierbare Objekte (z. b. Enumeratoren oder aktualisierbare Objekte) aktualisiert werden können.                                                                                                                                                                                      |
| [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)                                       | Wird von Clients und Anbietern für den Zugriff auf WMI-Dienste verwendet. Die-Schnittstelle wird nur von WMI implementiert und ist die primäre WMI-Schnittstelle.                                                                                                                                                                           |
| [**Iwbemstatus Code-Text**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemstatuscodetext)                           | Extrahiert Text Zeichenfolgen-Beschreibungen von Fehlercodes oder den Namen des Subsystems, in dem der Fehler aufgetreten ist.                                                                                                                                                                                                    |
| [**Iwbemunboundobjectsink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink)                     | Wird von allen logischen Ereignisconsumern implementiert. Es handelt sich um eine einfache Sink-Schnittstelle, die die Übermittlung von Ereignis Objekten akzeptiert.                                                                                                                                                                                          |



 

> [!Note]  
> Viele der WMI-com-Funktionen geben numerische Fehlercodes zurück, die als benannte Konstanten dokumentiert werden. Diese Konstanten werden in der Datei "wbemcli. h" im Ordner "PSDK WMI include" definiert \\ . Weitere Informationen finden Sie unter [WMI-Rückgabe Codes](wmi-return-codes.md).

 

Weitere Informationen zu den folgenden Themen für die COM-Programmierung finden Sie unter [Komponentenentwicklung]( /previous-versions//ee663263(v=vs.85)):

-   Schnittstellen und Objektdesign.
-   Implementieren von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).
-   Speicherverwaltung
-   Behandeln der Verweis Zählung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> </dl>

 

 
