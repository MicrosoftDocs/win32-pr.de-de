---
title: Beispiel Dienstanbieter
description: Beispiel Dienstanbieter
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Windows Media Device Manager, Beispiele
- Device Manager, Beispiele
- Windows Media Device Manager, Dienstanbieter Beispiel
- Beispiel für Device Manager, Dienstanbieter
- Dienstanbieter, Beispiele
- Beispiele, Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337369"
---
# <a name="sample-service-provider"></a>Beispiel Dienstanbieter

Das Windows Media Device Manager SDK enthält einen Beispiel Dienstanbieter, den Sie verwenden können. Dieser Dienstanbieter enthält eine-Klasse, die jede Festplatte auf dem Computer so meldet, als ob es sich um ein angefügtes Gerät handelt. Die einzige Anwendung, die diesen Dienstanbieter verwendet, ist die Beispielanwendung. Windows-Explorer wird die von diesem Dienstanbieter gemeldeten Geräte nicht sehen. Das Dienstanbieter Beispiel ist ein COM-Objekt, das auf ATL basiert. In den folgenden Schritten wird erläutert, wie der Beispiel Dienstanbieter verwendet wird:

> [!Note]  
> Der Beispiel Dienstanbieter implementiert sehr wenige Features und sollte daher nicht zum Testen von Windows Media Device Manager-Anwendungen verwendet werden. Um eine Anwendung zu testen, verwenden Sie einen vollständig implementierten Dienstanbieter.

 

-   Das Beispiel wurde mit einem Codierungsfehler ausgeliefert, der dazu führt, dass der Dienstanbieter nicht funktioniert. Um diesen Fehler zu beheben, öffnen Sie die Datei "mdspenumstorage. cpp", die im Ordner < *SDK-Installationspfad*  > \\ WMFSDK95 \\ WMDM \\ mdsp \\ mshdsp installiert ist, gehen Sie zu Zeile 185, und ändern Sie die folgende Zeile:

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

Folgendermaßen:

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  Kompilieren Sie die MsHDSP.dll Datei. Hierfür können Sie entweder NMAKE oder Visual Studio verwenden. Weitere Informationen zum Kompilieren der Anwendung finden Sie unter [Kompilieren des Beispiel Dienstanbieters mithilfe von NMAKE](compiling-the-sample-service-provider-using-nmake.md) oder [Kompilieren des Beispiel Dienstanbieters mithilfe von Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) .
2.  Registrieren Sie MsHDSP.dll mithilfe von regsvr32. Die folgende Zeile, die in ein Eingabe Aufforderungs Fenster in demselben Ordner wie MsHDSP.dll eingegeben wird, registriert den Beispiel Dienstanbieter:

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    Geben Sie an der Eingabeaufforderung die folgende Zeile ein, um die Identitätswechsel für ein Gerät zu verhindern:

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  Die Wechsel Datenträger, die von dieser DLL angenommen werden, können nur von der mit diesem SDK gelieferten Beispielanwendung eingesehen werden. Kompilieren Sie die Beispielanwendung mit einer der Methoden, die in Beispiel für eine [Desktop Anwendung](sample-desktop-application.md)beschrieben werden.
4.  Um den Dienstanbieter mit Visual Studio zu debuggen, öffnen Sie den Dienstanbieter in Visual Studio, und wählen Sie im Menü **Debuggen** die Option **starten** . Navigieren Sie im Popup Dialogfeld zur Beispielanwendung, die Sie im vorherigen Schritt erstellt haben, und klicken Sie auf **OK**, damit der Dienstanbieter im Debugmodus ausgeführt wird.

    Wenn Sie den Dienstanbieter ohne Debuggen in Visual Studio ausführen möchten, registrieren Sie einfach die msdhsp.dll, und führen Sie die im Lieferumfang des SDK enthaltene Beispiel-Desktop Anwendung aus Die Beispiel-Desktop Anwendung führt den Beispiel Dienstanbieter automatisch aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiele**](samples.md)
</dt> </dl>

 

 




