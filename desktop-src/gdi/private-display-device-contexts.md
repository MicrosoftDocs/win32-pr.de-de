---
description: Mit einem Privaten Gerätekontext kann eine Anwendung vermeiden, dass ein Anzeigegerätekontext jedes Mal abgerufen und initialisiert wird, wenn die Anwendung in einem Fenster zeichnen muss.
ms.assetid: 8de5a14b-a8b3-42a5-81f3-bf3c357052cb
title: Private Anzeigegerätekontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce63fddbc2e351b166308c9ca3ce674be1a0026851af7bb1192c49cc961cdee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092880"
---
# <a name="private-display-device-contexts"></a>Private Anzeigegerätekontexte

Mit einem *Privaten Gerätekontext* kann eine Anwendung vermeiden, dass ein Anzeigegerätekontext jedes Mal abgerufen und initialisiert wird, wenn die Anwendung in einem Fenster zeichnen muss. Private Gerätekontexte sind nützlich für Fenster, die viele Änderungen an den Werten der Attribute des Gerätekontexts erfordern, um sie für das Zeichnen vorzubereiten. Private Gerätekontexte reduzieren die Zeit, die für die Vorbereitung des Gerätekontexts erforderlich ist, und somit die Zeit, die zum Ausführen des Zeichnens im Fenster benötigt wird.

Eine Anwendung weist das System an, einen privaten Gerätekontext für ein Fenster zu erstellen, indem der CS \_ OWNDC-Stil in der Fensterklasse angegeben wird. Das System erstellt jedes Mal einen eindeutigen Privaten Gerätekontext, wenn es ein neues Fenster erstellt, das zur -Klasse gehört. Anfänglich hat der Private Device-Kontext die gleichen Standardwerte für Attribute wie ein allgemeiner Gerätekontext, aber die Anwendung kann diese jederzeit ändern. Das System behält Änderungen am Gerätekontext für die Lebensdauer des Fensters oder bis die Anwendung zusätzliche Änderungen vornimmt.

Eine Anwendung kann jederzeit nach dem Erstellen des Fensters mithilfe der [**GetDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdc) ein Handle für den Privaten Gerätekontext abrufen. Die Anwendung muss das Handle nur einmal abrufen. Danach kann das Handle beliebig oft beibehalten und verwendet werden. Da ein privater Gerätekontext nicht Teil des Anzeigegerätekontextcaches ist, muss eine Anwendung den Gerätekontext nie mithilfe der [**ReleaseDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-releasedc) freigeben.

Das System passt den Gerätekontext automatisch an, um Änderungen am Fenster widerzuspiegeln, z. B. verschieben oder dimensionieren. Dadurch wird sichergestellt, dass alle überlappenden Fenster immer ordnungsgemäß abgeschnitten werden. Das heißt, dass keine Aktion von der Anwendung erforderlich ist, um den Clipping sicherzustellen. Das System überarbeiten den Gerätekontext jedoch nicht so, dass er die Updateregion einschließt. Daher muss die Anwendung beim Verarbeiten einer [**WM \_ PAINT-Nachricht**](wm-paint.md) den Updatebereich entweder durch Aufrufen von [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) oder durch Abrufen des Updatebereichs und Durchschneiden mit dem aktuellen Clippingbereich integrieren. Wenn die Anwendung **BeginPaint** nicht aufruft, muss sie die Updateregion explizit mithilfe der [**ValidateRect-**](/windows/desktop/api/Winuser/nf-winuser-validaterect) oder [**ValidateRgn-Funktion**](/windows/desktop/api/Winuser/nf-winuser-validatergn) überprüfen. Wenn die Anwendung die Updateregion nicht überprüft, empfängt das Fenster eine endlose Reihe von **WM \_ PAINT-Meldungen.**

Da [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) das Caret-Zeichen ausblendet, wenn es in einem Fenster angezeigt wird, sollte eine Anwendung, die **BeginPaint** aufruft, auch die [**EndPaint-Funktion**](/windows/desktop/api/Winuser/nf-winuser-endpaint) aufrufen, um den Caretstrich wiederherzustellen. **EndPaint** hat keine anderen Auswirkungen auf den Kontext eines privaten Geräts.

Obwohl ein privater Gerätekontext praktisch zu verwenden ist, ist er hinsichtlich der Systemressourcen speicherintensiv, sodass 800 oder mehr Bytes gespeichert werden müssen. Private Gerätekontexte werden empfohlen, wenn Die Leistungsüberlegungen die Speicherkosten übersteigen.

Das System enthält den Kontext des privaten Geräts, wenn die [**WM \_ ERASEBKGND-Nachricht**](../winmsg/wm-erasebkgnd.md) an die Anwendung gesendet wird. Die aktuelle Auswahl des Privaten Gerätekontexts, einschließlich des Zuordnungsmodus, ist wirksam, wenn die Anwendung oder das System diese Nachrichten verarbeitet. Um unerwünschte Auswirkungen zu vermeiden, verwendet das System beim Löschen des Hintergrunds logische Koordinaten. Beispielsweise wird die [**GetClipBox-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox) verwendet, um die logischen Koordinaten des Zu löschenden Bereichs abzurufen, und diese Koordinaten werden an die [**FillRect-Funktion**](/windows/desktop/api/Winuser/nf-winuser-fillrect) übergeben. Anwendungen, die diese Nachrichten verarbeiten, können ähnliche Techniken verwenden.

Eine Anwendung kann die [**GetDCEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdcex) verwenden, um zu erzwingen, dass das System einen allgemeinen Gerätekontext für das Fenster zurückgibt, das über einen privaten Gerätekontext verfügt. Dies ist nützlich, um schnelle Toucheingaben zu einem Fenster durchzuführen, ohne die aktuellen Werte der Attribute des Privaten Gerätekontexts zu ändern.

 

 
