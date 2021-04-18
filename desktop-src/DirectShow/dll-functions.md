---
description: In diesem Thema wird beschrieben, wie eine Komponente in Microsoft DirectShow als Dynamic Link Library (dll) implementiert wird.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: DLL-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344772"
---
# <a name="dll-functions"></a>DLL-Funktionen

In diesem Thema wird beschrieben, wie eine Komponente in Microsoft DirectShow als Dynamic Link Library (dll) implementiert wird.

Eine DLL muss die folgenden Funktionen implementieren, damit Sie registriert, nicht registriert und in den Arbeitsspeicher geladen werden kann.

-   [*DllMain*](/windows/desktop/Dlls/dllmain): der DLL-Einstiegspunkt. Der Name *DllMain* ist ein Platzhalter für den Namen der Bibliothek definierten Funktion. Die DirectShow-Implementierung verwendet den Namen **DllEntryPoint**. Weitere Informationen finden Sie unter Platform SDK.
-   [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): erstellt eine klassenfactoryinstanz. Wird in den vorherigen Abschnitten beschrieben.
-   [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): fragt ab, ob die DLL sicher entladen werden kann.
-   [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): erstellt Registrierungseinträge für die dll.
-   [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): entfernt Registrierungseinträge für die dll.

Die ersten drei werden von DirectShow implementiert. Wenn Ihre Factoryvorlage eine Initialisierungsfunktion in der [**m \_ lpfninit**](cfactorytemplate-m-lpfninit.md) -Element Variablen bereitstellt, wird diese Funktion innerhalb der DLL-Einstiegspunkt Funktion aufgerufen. Weitere Informationen dazu, wann das System die DLL-Einstiegspunkt Funktion aufruft, finden Sie unter [*DllMain*](/windows/desktop/Dlls/dllmain).

Sie müssen [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)implementieren, aber DirectShow bietet eine Funktion mit dem Namen [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) , die die erforderliche Arbeit erledigt. Die Komponente kann diese Funktion einfach einschließen, wie im folgenden Beispiel gezeigt:


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



Allerdings können Sie in [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) den Registrierungsprozess nach Bedarf anpassen. Wenn Ihre DLL einen Filter enthält, müssen Sie möglicherweise zusätzliche Schritte ausführen. Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).

Exportieren Sie in der Modul Definitionsdatei (. def) alle DLL-Funktionen mit Ausnahme der Einstiegspunkt Funktion. Im folgenden finden Sie eine Beispieldatei für die DEF-Datei:


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



Sie können die DLL mit dem Regsvr32.exe-Hilfsprogramm registrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer DirectShow-Filter-dll](how-to-create-a-dll.md)
</dt> </dl>

 

 
