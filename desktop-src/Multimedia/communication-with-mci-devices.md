---
title: Kommunikation mit MCI-Geräten
description: Kommunikation mit MCI-Geräten
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- MCI-Geräte, kommunizieren
- Mciwndgetde viceid-Makro
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314709"
---
# <a name="communication-with-mci-devices"></a>Kommunikation mit MCI-Geräten

Für jedes MCI-Gerät ist es möglich, einen oder mehrere der folgenden als Bezeichner zu verwenden:

-   ein Geräte Bezeichner
-   ein Gerätename
-   Alias
-   der Dateiname des aktuell geladenen Inhalts.

Mciwnd bietet Makros, die Sie verwenden können, um diese Informationen abzurufen. Sie können diese Informationen dann verwenden, um direkt über MCI mit MCI-Geräten zu kommunizieren, die mciwnd-Fenstern zugeordnet sind.

Sie können den Bezeichner des aktuellen MCI-Geräts abrufen, indem Sie das [**mciwndgetdebug**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) -Makro verwenden. Der MCI-Geräte Bezeichner ist ein numerischer Wert, der die Instanz des MCI-Geräts identifiziert, das von Ihrer Anwendung verwendet wird. Die Anwendung kann diesen Bezeichner verwenden, wenn Sie mit einem MCI-Gerät über die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion kommunizieren.

Verwenden Sie das [**mciwndgetdevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) -Makro, um den Namen des aktuellen MCI-Geräts abzurufen. Der MCI-Gerätename ist eine NULL-terminierte Zeichenfolge, die den Gerätetyp identifiziert, der einem mciwnd-Fenster zugeordnet ist. Die Anwendung kann diesen Namen verwenden, wenn Sie mithilfe von **mciSendCommand** mit einem MCI-Gerät kommunizieren.

Sie können den Alias des aktuellen MCI-Geräts abrufen, indem Sie das Makro [**mciwndgetalias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) verwenden. Die Anwendung kann diesen Alias bei der Kommunikation mit einem MCI-Gerät mithilfe der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion verwenden.

Schließlich können Sie den Dateinamen abrufen, der von einem MCI-Gerät verwendet wird, indem Sie das [**mciwndgetfilename**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) -Makro verwenden. Der Dateiname identifiziert den aktuell einem mciwnd-Fenster zugeordneten Inhalt. Die Anwendung kann diesen Dateinamen bei der Kommunikation mit einem MCI-Gerät mithilfe von **mciSendCommand** oder **mciSendString** verwenden.

 

 