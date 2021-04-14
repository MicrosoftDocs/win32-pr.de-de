---
title: DPI_AWARENESS_CONTEXT handle (WINDEF. h)
description: Identifiziert den kontextkontext für ein Fenster.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340748"
---
# <a name="dpi_awareness_context-handle"></a>\_Kontext Handle für dpi-Informationen \_

Identifiziert den kontextkontext für ein Fenster.

## <a name="syntax"></a>Syntax

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a>Konstanten

**DPI \_ - \_ Kontext ist \_ nicht bekannt.**<dl> DPI ist nicht bekannt. Dieses Fenster wird nicht für dpi-Änderungen skaliert, und es wird immer angenommen, dass es einen Skalierungsfaktor von 100% (96 dpi) gibt. Sie wird automatisch durch das System auf jeder anderen dpi-Einstellung skaliert.  
</dl>

**\_ \_ Kontext System für \_ dpi-Bewusstsein \_**<dl> System-dpi-fähig. Dieses Fenster wird nicht für dpi-Änderungen skaliert. Es wird einmal eine Abfrage für den dpi-Wert durchführen und diesen Wert für die Lebensdauer des Prozesses verwenden. Wenn sich der dpi-Wert ändert, wird der Prozess nicht an den neuen dpi-Wert angepasst. Der Wert wird vom System automatisch zentral hoch-oder herunterskaliert, wenn der dpi-Wert vom System Wert geändert wird.  
</dl>

**DPI \_ - \_ Kontext \_ pro \_ Monitor \_**<dl> Pro Monitor-dpi-fähig. Dieses Fenster überprüft den dpi-Wert, wenn er erstellt wird, und passt den Skalierungsfaktor an, wenn sich der dpi-Wert ändert Diese Prozesse werden nicht automatisch vom System skaliert.  
</dl>

**DPI \_ - \_ kontextkontext \_ pro \_ Monitor- \_ Aware \_ v2**<dl> Wird auch als " **pro Monitor v2**" bezeichnet. Ein Fortschritt im Hinblick auf den ursprünglichen dpi-Modus für den dpi-Wert, mit dem Anwendungen auf einem Fenster der obersten Ebene auf neues dpi-bezogenes Skalierungs Verhalten zugreifen können.  
Pro Monitor v2 wurde im Creators Update von Windows 10 zur Verfügung gestellt und ist in früheren Versionen des Betriebssystems nicht verfügbar.  
Die folgenden zusätzlichen Verhaltensweisen werden eingeführt:

-   **Dpi-Änderungs Benachrichtigungen** für das untergeordnete Fenster: in pro Monitor v2-Kontexten wird die gesamte Fenster Struktur über alle auftretenden dpi-Änderungen benachrichtigt.
-   **Skalierung des nicht-Client Bereichs** : in allen Fenstern wird automatisch der nicht-Client-Bereich in einer dpi-sensiblen Weise gezeichnet. Aufrufe von [**enablenonclientdpiscalingsind**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) nicht erforderlich.
-   **Skalierung von Win32-Menüs** : alle Ntuser-Menüs, die in "pro Monitor v2"-Kontexten erstellt werden, werden pro Monitor skaliert.
-   **Dialog Feld Skalierung** : in den einzelnen Monitor v2-Kontexten erstellte Win32-Dialoge reagieren automatisch auf dpi-Änderungen.
-   **Verbesserte Skalierung von ComCtl32** -Steuerelementen: verschiedene ComCtl32-Steuerelemente haben ein verbessertes dpi-Skalierungs Verhalten in pro Monitor v2-Kontext
-   **Verbessertes Design Verhalten** : uxtheme-Handles, die im Kontext eines pro Monitor v2-Fensters geöffnet wurden, werden im Hinblick auf den dpi-Wert ausgeführt, der diesem Fenster zugeordnet ist.

  
</dl>

**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**

DPI-Informationen mit verbesserter Qualität von GDI-basiertem Inhalt. Dieser Modus verhält sich ähnlich wie DPI_AWARENESS_CONTEXT_UNAWARE, ermöglicht aber auch das automatische verbessern der renderingqualität von Text und anderen GDI-basierten primitiven, wenn das Fenster auf einem High-dpi-Monitor angezeigt wird.

Weitere Informationen finden Sie unter [verbessern der High-dpi-Oberfläche in GDI-basierten Desktop-Apps](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).

DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED wurde im Update von Windows 10 vom Oktober 2018 eingeführt (auch bekannt als Version 1809).


## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|----|-----------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1607, \[ nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt <br/>  |
| Header<br/>                   | <dl> <dt>WINDEF. h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Aredpiawareness contextsequal**](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[**Getawarenmefromdpiawarretecontext**](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[**Getdpifromdpiawareress Context**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[**Getthreaddpiawareress Context**](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[**Getwindowdpiawareress Context**](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[**Isvaliddpiawareress Context**](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[**Setprocessdpiawareress Context**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[**Setthreaddpiawareress Context**](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
