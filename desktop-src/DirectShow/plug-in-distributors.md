---
description: Plug-in-Verteiler
ms.assetid: 80ff713d-f704-40d3-9317-cbf33d932207
title: Plug-in-Verteiler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7817e5e31b29444cc596b0be583be2198adc018
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346814"
---
# <a name="plug-in-distributors"></a>Plug-in-Verteiler

Mit Plug-in-Verteilern (PIDs) können Sie die Funktionalität des Filter Graph-Managers erweitern. Ein Plug-in-Verteiler ist ein COM-Objekt, das der Filter Graph-Manager zur Laufzeit aggregiert. Anwendungen erhalten Zugriff auf die PID über den Filter Graph-Manager.

Wenn der Filter Graph-Manager nach einer Schnittstelle abgefragt wird, die er nicht unterstützt, durchsucht er die Registrierung nach einem Schlüssel mit der folgenden Form:


```C++
HKEY_CLASSES_ROOT\Interface\IID\Distributor
```



`IID` ist eine Zeichenfolge, die den Schnittstellen Bezeichner enthält. Wenn der Registrierungs Eintrag vorhanden ist, definiert der Wert des Eintrags den Klassen Bezeichner (CLSID) einer PID, die die Schnittstelle unterstützt. Der Filter Graph-Manager aggregiert die PID und gibt einen Schnittstellen Zeiger zurück, der als äußerer **IUnknown** für die PID fungiert. Wenn die Anwendung Methoden für die Schnittstelle aufruft, ruft Sie Sie tatsächlich auf der PID auf. Das vorhanden sein der PID ist jedoch für die Anwendung transparent.

Der Begriff *Verteiler* ergibt sich aus der Tatsache, dass eine PID ihren äußeren **IUnknown** -Zeiger für Schnittstellen im Filter Diagramm-Manager Abfragen kann. Durch Aufrufen der [**ifiltergraph:: enumfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) -Methode kann die PID die Filter im Diagramm auflisten und Methodenaufrufe an diese Filter verteilen. Auf diese Weise kann eine PID als einzelner Kontrollpunkt dienen, damit die Anwendung Methoden für Filter aufruft.

Wenn der Filter Graph-Manager eine PID aggregiert, fragt er die PID für die [**idistributor notify**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) -Schnittstelle ab. Wenn die PID diese Schnittstelle unterstützt, verwendet der Filter Graph-Manager Sie, um die PID über Änderungen im Diagramm zu benachrichtigen:

-   Wenn das Filter Diagramm zwischen den Zuständen "ausführen", "angehalten" und "beendet" wechselt, wird [**idistributornotify:: Run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run), [**idistributornotify::P ause**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause)oder [**idistributornotify:: Stopp**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop)aufgerufen.
-   Wenn eine Referenzuhr festgelegt ist, ruft der Filter Graph-Manager [**idistributornotify:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource)auf.
-   Wenn Filter hinzugefügt oder entfernt werden oder wenn Pin-Verbindungen geändert werden, ruft der Filter Graph-Manager [**idistributornotify:: notifygraphchange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange)auf.

Erstellen Sie ein COM-Objekt, das Aggregation unterstützt, um eine benutzerdefinierte PID zu implementieren. Es muss eine Schnittstelle unterstützen, die der Filter Graph-Manager nicht bereits unterstützt. Optional kann Sie die **idistributor notify** -Schnittstelle unterstützen.

Wenn die PID Schnittstellen Zeiger vom Filter Diagramm-Manager erhält, sollte Sie sofort freigegeben werden. Andernfalls könnte Sie einen Zirkel Verweis Zähler erstellen, wodurch verhindert werden kann, dass der Filter Graph-Manager zerstört wird. Das Speichern eines Verweis Zählers für den Filter Diagramm-Manager ist in jedem Fall unnötig, da der Filter Graph-Manager die Lebensdauer der PID steuert.

Da eine PID speziell für die Aggregation durch den Filter Graph-Manager entwickelt wurde, können Sie dies in der Konstruktormethode der PID erzwingen. Überprüfen Sie, ob der äußere **IUnknown** -Zeiger **null** ist. wenn dies der Fall ist, geben Sie den Fehlercode "VFW \_ E Owner" zurück \_ \_ . (Siehe [Fehler-und Erfolgs Codes](error-and-success-codes.md).) Außerdem können Sie den äußeren **IUnknown** -Zeiger für die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle Abfragen, um zu verhindern, dass andere Objekte die PID aggzieren. Gibt einen Fehlercode zurück, wenn das Objekt **igraphbuilder** nicht verfügbar macht.

 

 



