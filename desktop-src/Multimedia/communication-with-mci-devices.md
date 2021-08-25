---
title: Kommunikation mit MCI-Geräten
description: Kommunikation mit MCI-Geräten
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- MCI-Geräte, Kommunizieren
- MCIWndGetDeviceID-Makro
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd04187b948adf144a317a1d9eab80efb60bab8e7b05eaccffeb34722baa98a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785904"
---
# <a name="communication-with-mci-devices"></a>Kommunikation mit MCI-Geräten

Es ist möglich, dass jedes MCI-Gerät einen oder mehrere der folgenden Bezeichner verwendet:

-   Einen Gerätebezeichner
-   Einen Gerätenamen
-   ein Alias
-   der Dateiname des aktuell geladenen Inhalts.

MCIWnd stellt Makros bereit, mit deren Hilfe Sie diese Informationen abrufen können. Sie können diese Informationen dann verwenden, um über MCI direkt mit MCI-Geräten zu kommunizieren, die MCIWnd-Fenstern zugeordnet sind.

Sie können den Bezeichner des aktuellen MCI-Geräts mithilfe des [**MCIWndGetDeviceID-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) abrufen. Der MCI-Gerätebezeichner ist ein numerischer Wert, der die Instanz des von Ihrer Anwendung verwendeten MCI-Geräts identifiziert. Ihre Anwendung kann diesen Bezeichner bei der Kommunikation mit einem MCI-Gerät mithilfe der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) verwenden.

Verwenden Sie das [**MCIWndGetDevice-Makro,**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) um den Namen des aktuellen MCI-Geräts abzurufen. Der MCI-Gerätename ist eine auf NULL endende Zeichenfolge, die den Gerätetyp identifiziert, der einem MCIWnd-Fenster zugeordnet ist. Ihre Anwendung kann diesen Namen bei der Kommunikation mit einem MCI-Gerät mithilfe von **mciSendCommand** verwenden.

Sie können den Alias des aktuellen MCI-Geräts mithilfe des [**MCIWndGetAlias-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) abrufen. Ihre Anwendung kann diesen Alias bei der Kommunikation mit einem MCI-Gerät mithilfe der [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) verwenden.

Schließlich können Sie den von einem MCI-Gerät verwendeten Dateinamen mithilfe des [**MCIWndGetFileName-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) abrufen. Der Dateiname identifiziert den Inhalt, der derzeit einem MCIWnd-Fenster zugeordnet ist. Ihre Anwendung kann diesen Dateinamen bei der Kommunikation mit einem MCI-Gerät mithilfe von **mciSendCommand** oder **mciSendString** verwenden.

 

 