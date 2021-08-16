---
description: Der Zweck des Anbieterwrappers besteht darin, die (von den Smartcardherstellern bereitgestellten) COM-Schnittstellen auf niedriger Ebene für eine bestimmte Smartcard zu kapseln und zu verwenden. Diese Schnittstellen werden nicht von Microsoft bereitgestellt.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Anbieterwrapper-Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeec4a8a5125e8fe19201a6c810eb87705eb7b5614b49fb455e8a96af63c8d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785844"
---
# <a name="vendor-wrapper-service-provider"></a>Anbieterwrapper-Dienstanbieter

Der Zweck des Anbieterwrappers besteht darin, die (von den Smartcardherstellern bereitgestellten) COM-Schnittstellen auf niedriger Ebene für eine bestimmte Smartcard zu kapseln und zu verwenden. Diese Schnittstellen werden nicht von Microsoft bereitgestellt.

![Anbieterwrapper](images/scspart1.png)

Wie in Teil 6 der *Interoperabilitätsspezifikation für ICCs und Pc-Systeme* (siehe Spezifikationen unter ) beschrieben, [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ist die von diesem Wrapper verfügbar gemachte Funktionalität einfacher zu verwenden als die Funktionalität von vier separaten Dienstanbietern. Die Funktionalität des Wrappers kann in vier Hauptbereiche unterteilt werden:

-   Smartcard-Authentifizierungsdienste, z. B. Abrufen der Abfrage und Kartenauthentifizierung.
-   Smartcard-Dateizugriff oder Dateisystemdienste wie Öffnen, Schließen, Lesen und Schreiben.
-   Smartcardverwaltung, z. B. Anfügen und Trennen.
-   Smartcard-Überprüfungsdienste, z. B. Überprüfen und Ändern des Codes.

> [!Note]  
> Diese Spezifikation ist in einigen Sprachen und Ländern oder Regionen möglicherweise nicht verfügbar.

 

Die Funktionalität ist spezifisch für den Typ der verwendeten Karte (welche Funktionen die Karte unterstützt, Protokolle usw.) und unterscheidet sich für jede Karte.

Der Microsoft SCardCOM-Beispielwrapper verwendet die ATL-COM-Bibliothek, um einen einfachen Wrapper zu implementieren und eine Vorlage für andere Wrapper zu erstellen. Es implementiert die folgenden Schnittstellen.



| Schnittstelle oder Objekt                                     | Beschreibung                         |
|---------------------------------------------------------|-------------------------------------|
| [**ISCardAuth**](iscardauth.md)<br/>             | Authentifizierungsdienste.<br/> |
| [**ISCardFileAccess**](iscardfileaccess.md)<br/> | Dateisystemdienste.<br/>    |
| [**ISCardManage**](iscardmanage.md)<br/>         | Verwaltungsdienste.<br/>     |
| [**ISCardVerify**](iscardverify.md)<br/>         | Überprüfungsdienste.<br/>   |



 

> [!Note]  
> Das SCardCOM-Beispiel wird nur als Beispiel für die Implementierung der Wrapperschnittstellen bereitgestellt. Um DLL-Namenskonflikte mit anderen Anbietern zu vermeiden, dürfen Sie SCardCOM.dll nicht als Namen von DLLs verwenden, die Sie erstellen.

 

Es folgt eine typische Verwendung des Anbieterwrappers. In diesem Beispiel wird die [**ISCardManage-Schnittstelle**](iscardmanage.md) verwendet, um Instanzen der Schnittstellen zu erstellen, die vom Dienstanbieter umschlossen werden, und die [**ISCardVerify-Schnittstelle,**](iscardverify.md) um deren Betrieb zu überprüfen.

**So erstellen Sie einen Wrapper-Dienstanbieter**

1.  Erstellen Sie eine Instanz der [**ISCardManage-Schnittstelle.**](iscardmanage.md) Verwenden Sie diese Schnittstelle, um eine Instanz der erforderlichen Schnittstellen zu erstellen (z. B. [**ISCardFileAccess**](iscardfileaccess.md) oder [**ISCardVerify**](iscardverify.md)). Beim Erstellen dieser Schnittstellen werden auch alle entsprechenden COM-Schnittstellen auf niedriger Ebene erstellt.
2.  Anfügen/Herstellen einer Verbindung mit einer Karte über die entsprechende [**ISCardManage-Methode.**](iscardmanage.md)
3.  Führen Sie erforderliche Vorgänge über die entsprechende [**ISCardVerify-Methode**](iscardverify.md) aus (die möglicherweise mehrere COM-Schnittstellen und -Methoden auf niedriger Ebene aufruft, um sie abzuschließen).
4.  Wiederholen Sie dies für andere Vorgänge.
5.  Release nach Abschluss des Vorgangs.

Der Name der COM-Schnittstelle und der Schnittstellenbezeichner (GUID) dürfen sich nicht von denen ändern, die im Code oder Beispielwrapper verwendet werden. Die Klassen-GUID (d. h., in der sich eine tatsächliche Implementierung einer Schnittstelle befindet) muss jedoch von der verwendeten geändert werden. Dies ist besonders wichtig bei der Implementierung eines Anbieterwrappers. Ein Beispiel wäre die Verwendung mehrerer Anbieterwrapper auf einem bestimmten Computer. Diese Wrapper sollten die gleichen COM-Schnittstellen implementieren, verwenden jedoch immer unterschiedliche Implementierungsstrategien. Daher sind verschiedene Klassen (und Klassen-IDs) erforderlich.

 

 




