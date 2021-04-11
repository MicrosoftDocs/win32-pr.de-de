---
description: Der Hersteller Wrapper dient dazu, die COM-Schnittstellen auf niedriger Ebene (die von den Smartcardherstellern bereitgestellt werden) für eine bestimmte Smartcard zu kapseln und zu verwenden. Diese Schnittstellen werden nicht von Microsoft bereitgestellt.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Anbieter-Wrapper Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128905"
---
# <a name="vendor-wrapper-service-provider"></a>Anbieter-Wrapper Dienstanbieter

Der Hersteller Wrapper dient dazu, die COM-Schnittstellen auf niedriger Ebene (die von den Smartcardherstellern bereitgestellt werden) für eine bestimmte Smartcard zu kapseln und zu verwenden. Diese Schnittstellen werden nicht von Microsoft bereitgestellt.

![Hersteller Wrapper](images/scspart1.png)

Wie in Teil 6 der *Interoperabilitäts Spezifikation für ICCS und Personal Computer Systeme* (siehe Spezifikationen unter [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ) beschrieben, ist die Funktionalität, die von diesem Wrapper verfügbar gemacht wird, einfacher zu verwenden als die Funktionalität von vier separaten Dienstanbietern. Die Wrapper Funktion kann in vier Hauptbereiche unterteilt werden:

-   Dienste für die Smartcard-Authentifizierung, z. b. Get Challenge und Card Authentication.
-   Zugriff auf smartcarddateien oder Dateisystem Dienste, z. b. öffnen, schließen, lesen und schreiben.
-   Smartcardverwaltung, z. b. Anfügen und trennen.
-   Smartcard-Überprüfungs Dienste, z. b. überprüfen und Ändern von Code.

> [!Note]  
> Diese Spezifikation ist möglicherweise in einigen Sprachen und Ländern oder Regionen nicht verfügbar.

 

Die Funktionalität ist spezifisch für den Typ der verwendeten Karte (die von der Karte unterstützten Funktionen, Protokolle usw.) und unterscheidet sich für jede Karte.

Der Wrapper für den Microsoft scardcom-Beispiel verwendet die ATL-COM-Bibliothek, um einen einfachen Wrapper zu implementieren und eine Vorlage für andere Wrapper anzulegen. Die folgenden Schnittstellen werden implementiert.



| Schnittstelle oder Objekt                                     | BESCHREIBUNG                         |
|---------------------------------------------------------|-------------------------------------|
| [**Iscardauth**](iscardauth.md)<br/>             | Authentifizierungsdienste.<br/> |
| [**Iscardfileaccess**](iscardfileaccess.md)<br/> | Dateisystem Dienste.<br/>    |
| [**Iscardmanage**](iscardmanage.md)<br/>         | Verwaltungsdienste.<br/>     |
| [**Iscardverify**](iscardverify.md)<br/>         | Überprüfungs Dienste.<br/>   |



 

> [!Note]  
> Das Beispiel "scardcom" wird nur als Beispiel für das Implementieren der Wrapper Schnittstellen bereitgestellt. Um einen DLL-namens Konflikt mit anderen Anbietern zu vermeiden, dürfen Sie SCardCOM.dll nicht als Namen von DLLs verwenden, die Sie erstellen.

 

Im folgenden finden Sie eine typische Verwendung des Hersteller Wrappers. In diesem Beispiel wird die [**iscardmanage**](iscardmanage.md) -Schnittstelle verwendet, um Instanzen der Schnittstellen zu erstellen, die in den Dienstanbieter und die [**iscardverify**](iscardverify.md) -Schnittstelle integriert werden, um Ihren Vorgang zu überprüfen.

**So erstellen Sie einen Wrapper Dienstanbieter**

1.  Erstellen Sie eine Instanz der [**iscardmanage**](iscardmanage.md) -Schnittstelle. Verwenden Sie diese Schnittstelle, um eine Instanz der erforderlichen Schnittstellen (z. b. [**iscardfileaccess**](iscardfileaccess.md) oder [**iscardverify**](iscardverify.md)) zu erstellen. Wenn diese Schnittstellen erstellt werden, werden auch alle entsprechenden COM-Schnittstellen auf niedriger Ebene erstellt.
2.  Fügen Sie eine Karte mithilfe der entsprechenden [**iscardmanage**](iscardmanage.md) -Methode an/Stellen Sie eine Verbindung her.
3.  Führen Sie erforderliche Vorgänge über die entsprechende [**iscardverify**](iscardverify.md) -Methode aus (die möglicherweise mehrere COM-Schnittstellen auf niedriger Ebene aufruft, und Methoden zum Abschluss).
4.  Wiederholen Sie dies für andere Vorgänge.
5.  Release nach Abschluss des Vorgangs.

Der Name und der Schnittstellen Bezeichner (GUID) der COM-Schnittstelle dürfen sich nicht von den im Code-oder Beispiel Wrapper verwendeten Änderungen unterscheiden. Allerdings muss die Klassen-GUID (d. h., in der sich eine tatsächliche Implementierung einer Schnittstelle befindet) von den verwendeten geändert werden. Dies ist besonders wichtig, wenn ein Hersteller Wrapper implementiert wird. Ein Beispiel wäre die Verwendung mehrerer Hersteller-Wrapper auf einem bestimmten Computer. Diese Wrapper sollten die gleichen com-Schnittstellen implementieren, verwenden jedoch immer verschiedene Implementierungs Strategien. Daher sind verschiedene Klassen (und Klassen-IDs) erforderlich.

 

 




