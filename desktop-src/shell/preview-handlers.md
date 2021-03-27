---
description: Vorschau Handler werden aufgerufen, wenn ein Element ausgewählt wird, um eine vereinfachte, umfangreiche schreibgeschützte Vorschau der Dateiinhalte im Lesebereich der Sicht anzuzeigen. Dies geschieht, ohne dass die zugehörige Anwendung der Datei gestartet wird.
ms.assetid: 166a4001-d237-44a4-a457-e320e995639c
title: Vorschau Handler und Shell-Vorschau Host
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993c6c8e7b15d9bfc24b5dd42352407a3a53c45b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979960"
---
# <a name="preview-handlers-and-shell-preview-host"></a>Vorschau Handler und Shell-Vorschau Host

Vorschau Handler werden aufgerufen, wenn ein Element ausgewählt wird, um eine vereinfachte, umfangreiche Schreib *geschützte Vorschau der* Dateiinhalte im Lesebereich der Sicht anzuzeigen. Dies geschieht, ohne dass die zugehörige Anwendung der Datei gestartet wird.

In diesem Thema werden die folgenden Themen behandelt:

-   [Vorschau der handlerarchitektur](#preview-handler-architecture)
-   [Server Modell Optionen](#server-model-options)
-   [Initialisierung](#initialization)
-   [Vorschauhandlerdatenfluss](#preview-handler-data-flow)
-   [Debuggen eines Vorschau Handlers](#debugging-a-preview-handler)
-   [Bereitstellen eines eigenen Prozesses für einen Vorschau Handler](#providing-your-own-process-for-a-preview-handler)
-   [Zugehörige Themen](#related-topics)

## <a name="preview-handler-architecture"></a>Vorschau der handlerarchitektur

Ein Vorschau Handler ist eine gehostete Anwendung. Zu den Hosts gehören Windows-Explorer in Windows Vista oder Microsoft Outlook 2007. Hosts implementieren [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) als Kommunikationsmethode zwischen dem Vorschau Handler und dem Host.

Der Vorschau Handler implementiert die folgenden Schnittstellen:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
-   [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
-   [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) (optional)

Der Handler wird über seine [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)aufgerufen, die einen [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger zurückgibt, über den Sie ein [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) -Objekt für die Interaktion mit dem Host anfordern.

## <a name="server-model-options"></a>Server Modell Optionen

Vorschau Handler werden immer außerhalb des Prozesses ausgeführt. Hierfür gibt es zwei Methoden:

1.  Ein Vorschau Handler kann als Prozess interner Server erstellt, aber über einen Out-of-Process-Ersatz Host ausgeführt werden. Dies ist die bevorzugte Methode. Das System stellt einen Ersatz Zeichen Host für dieses in der Prevhost.exe-Datei bereit. Vorschau Handler, die mit dieser Methode erstellt wurden, sind nicht mit Outlook 2007 unter Windows XP kompatibel. Diese Handler funktionieren jedoch in Windows-Explorer und Outlook 2007, die unter Windows Vista ausgeführt werden.
2.  Ein Vorschau Handler kann als lokaler Component Object Model (com)-Server erstellt werden. Dies wird aus verschiedenen Gründen nicht empfohlen. Zuerst ist die Implementierung eines Prozess internen Servers einfacher. Noch wichtiger ist, dass die Implementierung als Prozess interner Server eine bessere Kontrolle über die Lebensdauer des Handlerobjekts bietet, was eine bessere Bereinigung und Effizienz ermöglicht.

Standardmäßig werden Vorschau Handler aus Sicherheitsgründen in einem Il-Prozess mit niedriger Integritäts Ebene ausgeführt. Optional können Sie die Ausführung als Low-Il-Prozess deaktivieren, indem Sie den folgenden Wert in der Registrierung festlegen. Dies wird jedoch nicht empfohlen. Systeme können schließlich so konfiguriert werden, dass Sie jeden Prozess ablehnen, bei dem es sich nicht um niedrige Il handelt

```
HKEY_CLASSES_ROOT
   CLSID
      {YOUR HANDLER'S CLSID}
         DisableLowILProcessIsolation [DWORD] = 1
```

Verschiedene Vorschau Handler verwenden den gleichen ProzessStandard mäßig gemeinsam. Zwei Instanzen von Prevhost.exe können gleichzeitig ausgeführt werden. eine für Handler, die als Low-Il-Prozesse ausgeführt werden, eine für Handler, die dieses Verhalten deaktiviert haben.

## <a name="initialization"></a>Initialisierung

Wie bei Miniaturansichten und Eigenschaften Handlern wird dringend empfohlen, dass Sie den Handler mit einem Stream initialisieren. Wenn erforderlich, können Sie eine Datei oder ein Element initialisieren, aber Streams bieten die sicherste Methode zum Implementieren eines Handlers. Durch die Initialisierung durch einen Stream wird die Datei Integrität und die Stabilitäts Vorteile für das System der Ausführung des Handlers als Low-Il-Prozess sichergestellt, wie z. b. das Schützen des Systems vor Pufferüberläufen, das Einschränken des Speicher Orts von Informationen und das Einschränken der Kommunikation mit anderen Fenstern.

Wenn Sie mit einem Datei-oder shellelement initialisieren müssen, speichern Sie den Dateipfad oder einen Verweis auf das [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)-Element. Lesen Sie keine Daten aus diesen Quellen, bis [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) aufgerufen wird.

Im Allgemeinen sollten bei der Initialisierung keine schweren Aufgaben ausgeführt werden, z. b. das Erstellen und Speichern eines Vorschau Bilds. Zur optimalen Effizienz sollte diese Art der Verarbeitung erst durchgeführt werden, wenn die Vorschau für aufgerufen wird.

## <a name="preview-handler-data-flow"></a>Vorschauhandlerdatenfluss

Der Datenfluss im Vorschau Prozess folgt dem hier gezeigten allgemeinen Pfad. Der Host kann als Windows-Explorer in Windows Vista oder Outlook 2007 betrachtet werden.

1.  Der Vorschau Handler wird initialisiert, vorzugsweise mit einem Stream.
2.  Das Ansichts Fenster wird vom Host über [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow)an den Handler übermittelt.
3.  An diesem Punkt sollte der Handler nichts weiter tun, bis [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) aufgerufen wird.
4.  Die Vorschau wird im Lesebereich durch einen [**IPreviewHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview)-Ansichts Vorgang angezeigt::D opreview.
5.  Die Größe des Fensters wird über [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)festgelegt.
6.  Die Größe des Fensters wird bei Bedarf über [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)geändert.
7.  Die Vorschau wird entladen, und ihre Ressourcen werden freigegeben, wenn Sie nicht mehr benötigt werden, und zwar durch einen [**IPreviewHandler:: Entladen**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload)-Ansichts Vorgang.

## <a name="debugging-a-preview-handler"></a>Debuggen eines Vorschau Handlers

Wenn Sie die Empfehlungen zum Implementieren Ihres Vorschau Handlers als Prozess interner Server befolgt haben, können Sie an Prevhost.exe anfügen, um den Vorschau Handler zu debuggen. Wie bereits erwähnt, beachten Sie, dass es möglicherweise zwei Instanzen von Prevhost.exe gibt, eine für normale Low-Il-Prozesse und eine für die Handler, die die Ausführung als Low-Il-Prozess deaktiviert haben.

Wenn Sie Prevhost.exe nicht in der Liste der verfügbaren Prozesse finden, wurde es wahrscheinlich nicht zu diesem Zeitpunkt geladen. Wenn Sie auf eine Datei für eine Vorschau klicken, wird das Ersatz Zeichen geladen, und es sollte dann als anfügbare Prozess angezeigt werden.

## <a name="providing-your-own-process-for-a-preview-handler"></a>Bereitstellen eines eigenen Prozesses für einen Vorschau Handler

Wenn Sie die Erstellung eines neuen Prozesses für den Handler erzwingen möchten, anstatt ihn unter dem Standardprozess zu ausführen, erstellen Sie unter **AppID** einen neuen Unterschlüssel für Ihren Handler, und legen Sie dessen dllersatz-Eintrag auf "Prevhost.exe" fest. Verwenden Sie den **AppID** -Unterschlüssel anstelle der Standard-Prevhost.exe- **AppID**.

Wenn Sie einen neuen Prozess bereitstellen, kann der Handler die Ausführung unter einem freigegebenen Prozess vermeiden, da dies standardmäßig der Fall wäre. Dadurch können Sie beispielsweise die spezifische Version des Common Language Runtime (CLR) im Prozess sicherstellen. Dies ist erforderlich, wenn Sie eine verwaltete Implementierung eines Vorschau Handlers entwickeln.

> [!Note]  
> 32-Bit-Vorschau Handler sollten bei der Installation auf 64-Bit-Betriebssystemen **AppID** {534a1e02-d58fi-44fi0-b58b-36cbed287c7c} verwenden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Vorschau Handlern](building-preview-handlers.md)
</dt> <dt>

[Registrieren eines Vorschau Handlers](how-to-register-a-preview-handler.md)
</dt> <dt>

[Vorschau der handlerrichtlinien](preview-handler-guidelines.md)
</dt> </dl>

 

 
