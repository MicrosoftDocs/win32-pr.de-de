---
description: Vorschauhandler werden aufgerufen, wenn ein Element ausgewählt wird, um eine einfache, umfassende, schreibgeschützte Vorschau des Dateiinhalts im Lesebereich der Ansicht anzuzeigen. Dies erfolgt, ohne die zugeordnete Anwendung der Datei zu starten.
ms.assetid: 166a4001-d237-44a4-a457-e320e995639c
title: Vorschauhandler und Shell-Vorschauhost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ccc6c2a519b4f9646e76a0a0ef4d0d26348e08d114eb9a080aaee09a75b9f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858762"
---
# <a name="preview-handlers-and-shell-preview-host"></a>Vorschauhandler und Shell-Vorschauhost

Vorschauhandler werden aufgerufen, wenn ein Element ausgewählt *wird,* um eine einfache, umfassende, schreibgeschützte Vorschau des Dateiinhalts im Lesebereich der Ansicht anzuzeigen. Dies erfolgt, ohne die zugeordnete Anwendung der Datei zu starten.

In diesem Thema werden die folgenden Themen erläutert:

-   [Vorschauhandlerarchitektur](#preview-handler-architecture)
-   [Servermodelloptionen](#server-model-options)
-   [Initialisierung](#initialization)
-   [Preview Handler Data Flow](#preview-handler-data-flow)
-   [Debuggen eines Vorschauhandlers](#debugging-a-preview-handler)
-   [Bereitstellen eines eigenen Prozesses für einen Vorschauhandler](#providing-your-own-process-for-a-preview-handler)
-   [Zugehörige Themen](#related-topics)

## <a name="preview-handler-architecture"></a>Vorschauhandlerarchitektur

Ein Vorschauhandler ist eine gehostete Anwendung. Hosts enthalten den Windows Explorer in Windows Vista oder Microsoft Outlook 2007. Hosts implementieren [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) als Kommunikationsmethode zwischen dem Vorschauhandler und dem Host.

Der Vorschauhandler selbst implementiert diese Schnittstellen:

-   [**Iinitializewithstream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**Iobjectwithsite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
-   [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
-   [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) (optional)

Ihr Handler wird über das [**IObjectWithSite-Objekt**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)aufgerufen, das einen [**IUnknown-Zeiger**](/windows/win32/api/unknwn/nn-unknwn-iunknown) zurückgibt, über den Sie ein [**IPreviewHandlerFrame-Objekt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) für die Interaktion mit dem Host anfordern.

## <a name="server-model-options"></a>Servermodelloptionen

Für Vorschauhandler ist der Prozess immer nicht mehr verfügbar. Es gibt zwei Methoden, dies zu implementieren:

1.  Ein Vorschauhandler kann als Prozessserver erstellt, aber über einen Out-of-Process-Ersatzhost ausgeführt werden. Dies ist die bevorzugte Methode. Das System stellt einen Ersatzhost für diesen in der Prevhost.exe zurEntschlüsselung. Vorschauhandler, die mit dieser Methode erstellt werden, sind nicht mit Outlook 2007 auf Windows XP kompatibel. Diese Handler funktionieren jedoch in Windows Explorer und Outlook 2007 unter Windows Vista.
2.  Ein Vorschauhandler kann als lokaler serverseitiger Component Object Model (COM) erstellt werden. Dies wird aus verschiedenen Gründen nicht empfohlen. Erstens ist die Implementierung eines Prozessservers einfacher. Noch wichtiger ist, dass die Implementierung als Prozessserver eine bessere Kontrolle über die Lebensdauer des Handlerobjekts bietet, was eine bessere Bereinigung und Effizienz ermöglicht.

Standardmäßig werden Vorschauhandler aus Sicherheitsgründen in einem Il-Prozess (Low Integrity Level) ausgeführt. Sie können die Ausführung optional als Prozess mit niedriger IL deaktivieren, indem Sie den folgenden Wert in der Registrierung festlegen. Dies wird jedoch nicht empfohlen. Systeme könnten schließlich so konfiguriert werden, dass alle Prozesse abgelehnt werden, die keine geringe IL sind.

```
HKEY_CLASSES_ROOT
   CLSID
      {YOUR HANDLER'S CLSID}
         DisableLowILProcessIsolation [DWORD] = 1
```

Verschiedene Vorschauhandler verwenden standardmäßig denselben Prozess. Zwei Instanzen von Prevhost.exe können gleichzeitig ausgeführt werden. einer für Handler, die als Low IL-Prozesse ausgeführt werden, einer für Handler, die sich von diesem Verhalten abgemeldet haben.

## <a name="initialization"></a>Initialisierung

Wie bei Miniaturansichts- und Eigenschaftshandlern wird dringend empfohlen, den Handler mit einem Stream zu initialisieren. Sie können bei Bedarf über eine Datei oder ein Element initialisieren, aber Streams bieten die sicherste Möglichkeit, einen Handler zu implementieren. Die Initialisierung über einen Stream stellt die Dateiintegrität und die Stabilitätsvorteile für das System sicher, bei dem der Handler als niedriger IL-Prozess ausgeführt wird, z. B. der Schutz des Systems vor Pufferüberläufen, das Einschränken, wo ein Handler Informationen schreiben kann, und das Einschränken der Kommunikation mit anderen Fenstern.

Wenn Sie mit einer Datei oder einem Shellelement initialisieren müssen, speichern Sie den Dateipfad oder einen Verweis auf [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem). Lesen Sie erst Dann Daten aus diesen Quellen, wenn [**IPreviewHandler::D oPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) aufgerufen wird.

Im Allgemeinen sollte die Initialisierung keine hohen Arbeitslasten wie das Erstellen und Speichern eines Vorschauimages haben. Um eine optimale Effizienz zu erzielen, sollte diese Art der Verarbeitung erst erfolgen, wenn die Vorschau aufgerufen wird.

## <a name="preview-handler-data-flow"></a>Preview Handler Data Flow

Der Datenfluss im Vorschauprozess folgt dem hier gezeigten allgemeinen Pfad. Der Host kann als Windows Explorer in Windows Vista oder Outlook 2007 verwendet werden.

1.  Der Vorschauhandler wird initialisiert, vorzugsweise mit einem Stream.
2.  Das Ansichtsfenster wird vom Host über [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow)an den Handler übergeben.
3.  An diesem Punkt sollte der Handler nichts weiter tun, bis [**IPreviewHandler::D oPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) aufgerufen wird.
4.  Die Vorschau wird im Lesebereich durch einen Aufruf von [**IPreviewHandler::D oPreview angezeigt.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview)
5.  Die Größe des Fensters wird über [**IPreviewHandler::SetRect festgelegt.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)
6.  Die Größe des Fensters wird bei Bedarf über [**IPreviewHandler::SetRect geändert.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)
7.  Die Vorschau wird entladen, und ihre Ressourcen werden freigegeben, wenn sie nicht mehr benötigt werden, durch einen Aufruf von [**IPreviewHandler::Unload**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload).

## <a name="debugging-a-preview-handler"></a>Debuggen eines Vorschauhandlers

Wenn Sie die Empfehlungen befolgt haben, um den Vorschauhandler als Prozessserver zu implementieren, können Sie zum Debuggen des Vorschauhandlers an Prevhost.exe. Wie bereits erwähnt, sollten Sie beachten, dass es zwei Instanzen von Prevhost.exe geben könnte: eine für normale Prozesse mit niedriger IL und eine für die Handler, die sich gegen die Ausführung als niedriger IL-Prozess entschieden haben.

Wenn Sie die Prevhost.exe in der Liste der verfügbaren Prozesse nicht finden, wurde sie wahrscheinlich zu diesem Zeitpunkt nicht geladen. Wenn Sie auf eine Datei für eine Vorschau klicken, wird das Ersatzzeichen geladen, und es sollte dann als anfingbarer Prozess angezeigt werden.

## <a name="providing-your-own-process-for-a-preview-handler"></a>Bereitstellen eines eigenen Prozesses für einen Vorschauhandler

Wenn Sie die Erstellung eines neuen Prozesses für Ihren Handler erzwingen möchten, anstatt unter dem Standardprozess ausgeführt zu werden, erstellen Sie einen neuen Unterschlüssel für den Handler unter **AppID,** und legen Sie dessen DllSurrogate-Eintrag auf "Prevhost.exe" fest. Verwenden Sie **diesen AppID-Unterschlüssel** anstelle des Prevhost.exe **AppID**.

Durch die Bereitstellung eines neuen Prozesses kann der Handler vermeiden, dass er wie standardmäßig unter einem freigegebenen Prozess ausgeführt wird. Dadurch können Sie beispielsweise die spezifische Version der Common Language Runtime (CLR) im Prozess sicherstellen. Dies ist erforderlich, wenn Sie eine verwaltete Implementierung eines Vorschauhandlers erstellen.

> [!Note]  
> 32-Bit-Vorschauhandler sollten **appID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} verwenden, wenn sie auf 64-Bit-Betriebssystemen installiert sind.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Vorschauhandlern](building-preview-handlers.md)
</dt> <dt>

[Registrieren eines Vorschauhandlers](how-to-register-a-preview-handler.md)
</dt> <dt>

[Richtlinien für Vorschauhandler](preview-handler-guidelines.md)
</dt> </dl>

 

 
