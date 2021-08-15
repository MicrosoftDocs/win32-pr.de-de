---
description: In diesem Thema wird beschrieben, wie eine Komponente als Dll (Dynamic Link Library) in Microsoft DirectShow implementiert wird.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: DLL-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8c10951c63e14656fa967693145444c5d5fbffd96a2b11fa9ae4201ac89ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821084"
---
# <a name="dll-functions"></a>DLL-Funktionen

In diesem Thema wird beschrieben, wie eine Komponente als Dll (Dynamic Link Library) in Microsoft DirectShow implementiert wird.

Eine DLL muss die folgenden Funktionen implementieren, damit sie registriert, nicht registriert und in den Arbeitsspeicher geladen werden kann.

-   [*DllMain:*](/windows/desktop/Dlls/dllmain)Der DLL-Einstiegspunkt. Der Name *DllMain* ist ein Platzhalter für den bibliotheksdefinierte Funktionsnamen. Die DirectShow-Implementierung verwendet den Namen **DllEntryPoint.** Weitere Informationen finden Sie im Plattform-SDK.
-   [**DllGetClassObject:**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject)Erstellt eine Klassenfactoryinstanz. In den vorherigen Abschnitten beschrieben.
-   [**DllCanUnloadNow:**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)Fragt ab, ob die DLL sicher entladen werden kann.
-   [**DllRegisterServer:**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)Erstellt Registrierungseinträge für die DLL.
-   [**DllUnregisterServer:**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)Entfernt Registrierungseinträge für die DLL.

Von diesen werden die ersten drei von DirectShow implementiert. Wenn Ihre Factoryvorlage eine Initialisierungsfunktion in der [**Membervariable m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md) bereitstellt, wird diese Funktion aus der DLL-Einstiegspunktfunktion aufgerufen. Weitere Informationen dazu, wann das System die DLL-Einstiegspunktfunktion aufruft, finden Sie unter [*DllMain*](/windows/desktop/Dlls/dllmain).

Sie müssen [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)implementieren. DirectShow stellt jedoch eine Funktion namens [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) bereit, die die erforderlichen Aufgaben übernimmt. Ihre Komponente kann diese Funktion einfach umschließen, wie im folgenden Beispiel gezeigt:


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



In [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) können Sie den Registrierungsprozess jedoch nach Bedarf anpassen. Wenn Ihre DLL einen Filter enthält, müssen Sie möglicherweise zusätzliche Arbeit leisten. Weitere Informationen finden Sie unter [Registrieren von DirectShow-Filtern.](how-to-register-directshow-filters.md)

Exportieren Sie in der Datei module-definition (.def) alle DLL-Funktionen mit Ausnahme der Einstiegspunktfunktion. Im Folgenden wird eine DEF-Beispieldatei beschrieben:


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



Sie können die DLL mit dem hilfsprogramm Regsvr32.exe registrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md)
</dt> </dl>

 

 
