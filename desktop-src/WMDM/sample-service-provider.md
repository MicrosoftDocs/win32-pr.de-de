---
title: Beispiel-Dienstanbieter
description: Beispiel-Dienstanbieter
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Windows Medien Geräte-Manager,Beispiele
- Geräte-Manager,Beispiele
- Windows Medien Geräte-Manager,Beispiel für Dienstanbieter
- Geräte-Manager,Dienstanbieterbeispiel
- Dienstanbieter,Beispiele
- Beispiele,Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eead5296a1ba3213f291027c0b1e4d50275497ad2ebe5a3feaea994e4a5c8e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004910"
---
# <a name="sample-service-provider"></a>Beispiel-Dienstanbieter

Das Windows Media Geräte-Manager SDK enthält einen Beispieldienstanbieter, den Sie verwenden können. Dieser Dienstanbieter enthält eine Klasse, die jede Festplatte auf dem Computer so meldet, als wäre sie ein angeschlossenes Gerät. Die einzige Anwendung, die diesen Dienstanbieter verwendet, ist die Beispielanwendung. Windows Im Explorer werden die von diesem Dienstanbieter gemeldeten "Geräte" nicht angezeigt. Das Dienstanbieterbeispiel ist ein COM-Objekt, das auf ATL basiert. In den folgenden Schritten wird die Verwendung des Beispieldienstanbieters erläutert:

> [!Note]  
> Der Beispieldienstanbieter implementiert nur sehr wenige Features und sollte daher nicht zum Testen von Windows Media Geräte-Manager verwendet werden. Verwenden Sie zum Testen einer Anwendung einen vollständig implementierten Dienstanbieter.

 

-   Das Beispiel wurde mit einem Codierungsfehler ausgeliefert, der zu einer Fehlfunktion des Dienstanbieters führen wird. Öffnen Sie zum Beheben dieses Fehlers die Datei MDSPEnumStorage.cpp, die im Ordner < SDK-Installationspfad   > \\ WMFSDK95 WMDM mdsp mshdsp installiert ist, wechseln Sie zu Zeile \\ \\ 185, und ändern Sie die \\ folgende Zeile:

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

Folgendermaßen:

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  Kompilieren Sie MsHDSP.dll Datei. Hierzu können Sie entweder NMAKE oder Visual Studio. Informationen zum Kompilieren der Anwendung finden Sie unter [Kompilieren](compiling-the-sample-service-provider-using-visual-studio.md) des Beispieldienstanbieters mithilfe von [NMAKE](compiling-the-sample-service-provider-using-nmake.md) oder Kompilieren des Beispieldienstanbieters mit Visual Studio Kompilieren der Anwendung.
2.  Registrieren MsHDSP.dll mit regsvr32. In der folgenden Zeile, die in ein Eingabeaufforderungsfenster im gleichen Ordner wie MsHDSP.dll, wird der Beispieldienstanbieter registriert:

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    Um die Identität eines Geräts zu beenden, geben Sie an der Eingabeaufforderung die folgende Zeile ein:

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  Die Wechselmedien, deren Identität von dieser DLL angenommen wird, können nur von der Beispielanwendung angezeigt werden, die mit diesem SDK ausgeliefert wird. Kompilieren Sie die Beispielanwendung mithilfe einer der unter [Beispieldesktopanwendung beschriebenen Methoden.](sample-desktop-application.md)
4.  Öffnen Sie zum Debuggen des Dienstanbieters mit Visual Studio den Dienstanbieter in Visual Studio und wählen Sie **im** **Menü Debuggen die Option Starten** aus. Navigieren Sie im Popupdialogfeld zu der Beispielanwendung, die Sie im vorherigen Schritt erstellt haben, und klicken Sie auf **OK,** und der Dienstanbieter wird im Debugmodus ausgeführt.

    Um den Dienstanbieter ohne Debuggen in Visual Studio ausführen zu können, registrieren Sie einfach die msdhsp.dll und führen die Beispieldesktopanwendung aus, die im SDK enthalten ist. Die Beispieldesktopanwendung führt den Beispieldienstanbieter automatisch aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiele**](samples.md)
</dt> </dl>

 

 




