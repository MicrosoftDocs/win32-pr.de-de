---
title: Vorsichtsmaßnahmen für In-Context Hookfunktionen
description: Aus Leistungsgründen registrieren Cliententwickler Kontexthookfunktionen.
ms.assetid: 14b48920-a291-4519-b005-e559263a0e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1333cf7718ff954217170e89dce2af70cc081fcca18929282f6db4a188125b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565588"
---
# <a name="in-context-hook-function-precautions"></a>Vorsichtsmaßnahmen für In-Context Hookfunktionen

Aus Leistungsgründen registrieren Cliententwickler Kontexthookfunktionen. Da diese Hookfunktionen jedoch dem Adressraum des Servers zugeordnet sind, müssen Client- und Serverentwickler Vorsichtsmaßnahmen ergreifen, um sicherzustellen, dass die Ereignisverarbeitung reibungslos verläuft.

## <a name="precautions-for-client-developers"></a>Vorsichtsmaßnahmen für Cliententwickler

Cliententwickler sollten sich der folgenden Probleme bewusst sein:

-   Hookfunktionen im Kontext sollten nicht viel Prozessorzeit verwenden, da die Hookfunktion zurückgeben muss, bevor die Serveranwendung fortgesetzt wird.
-   Nachdem ein Ereignis ausgelöst wurde, ist es möglich, dass das einem Ereignis zugeordnete Fenster zum Zeitpunkt des Aufrufs der Hookfunktion nicht mehr vorhanden ist. Clients müssen überprüfen, ob das einem Ereignis zugeordnete Fenster noch vorhanden ist, bevor sie eine andere Aktion im Zusammenhang mit dem Ereignis ergreifen. Um sicherzustellen, dass ein Fenster noch vorhanden ist, verwenden Clients die Microsoft Win32 [**IsWindow-Funktion.**](/windows/desktop/api/winuser/nf-winuser-iswindow)
-   Wenn die DLL, in der die Hookfunktion definiert ist, mit einer anderen DLL verknüpft ist, müssen Cliententwickler sicherstellen, dass das System die andere DLL lädt. Bei impliziter Verknüpfung (mit DEF-Dateien und Importen) muss sich die zusätzliche DLL entweder im Windows Verzeichnis oder in einem der Systemverzeichnisse wie Windows \\ System, Windows \\ System32 oder Windows \\ SysWOW64 befinden. Bei expliziter Verknüpfung (mit [**LoadLibrary)**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)muss der vollständige Pfad zu dem Verzeichnis, in dem sich die zusätzliche DLL befindet, im Aufruf von **LoadLibrary** angegeben werden.
-   Hookfunktionen im Kontext können einen Stapelüberlauf verursachen, wenn die DLL, die die Hookfunktion enthält, in eine 16-Bit-Anwendung geladen wird. Dieses Problem tritt auf, weil 16-Bit-Anwendungen eine feste Stapelgröße verwenden, die nicht groß genug ist, um die Kette von Systemfunktionsaufrufen aufzunehmen, die zu einem Aufruf der Hookfunktion führen.

## <a name="precautions-for-server-developers"></a>Vorsichtsmaßnahmen für Serverentwickler

Serverentwickler müssen beachten, dass Clientanwendungen möglicherweise Kontexthookfunktionen registrieren. Wenn ein Server [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)aufruft, muss er darauf vorbereitet sein, [**WM \_ GETOBJECT**](wm-getobject.md) und andere [**IAccessible-Methoden**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) zu verarbeiten.

## <a name="invalid-interface-pointers"></a>Ungültige Schnittstellenzeiger

Wenn ein Client [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) innerhalb einer Kontexthookfunktion aufruft, zeigt der IAccessible-Schnittstellenzeiger, der zurückgegeben wird, direkt auf Code im Adressraum des Servers. [](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Wenn der Client eine Schnittstelleneigenschaft mit diesem Zeiger aufruft, ist die Component Object Model -Bibliothek (COM) nicht mit dem Marshalling (Packen und Senden von Schnittstellenparametern über Prozessgrenzen) oder dem Entmarshaling (Entpacken von Parametern, die über Prozessgrenzen hinweg gesendet wurden) beteiligt und erkennt nicht, ob ein Objekt zerstört wird.

Wenn der Client eine Schnittstelleneigenschaft für ein Objekt aufruft, das zerstört wird, verursacht der ungültige Schnittstellenzeiger einen General Protection-Fehler im Adressraum des Servers, es sei denn, der Server erkennt diese Situation.

Zum Schutz vor ungültigen Schnittstellenzeigern erstellen Server [Proxyobjekte,](creating-proxy-objects.md) die barrierefreie Objekte umschließen und die Lebensdauer barrierefreier Objekte überwachen. Wenn beispielsweise ein Client eine [**IAccessible-Eigenschaft**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) aufruft, um Informationen zu einem Objekt abzurufen, überprüft der Proxy, ob das barrierefreie Objekt noch verfügbar ist, und leitet in diesem Fall die Anforderung des Clients an das barrierefreie Objekt weiter. Wenn das barrierefreie Objekt zerstört wird, gibt der Proxy einen Fehler an den Client zurück.

 

 