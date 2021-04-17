---
title: Registrieren eines Dienstanbieter
description: Wenn Sie Ihren Dienst der Liste der Anbieter im Webpublishing-Assistenten oder im Assistenten für die Online-druckbestellung hinzufügen möchten, müssen Sie den entsprechenden Schlüssel und seine Werte der Windows-Registrierung hinzufügen.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- registrieren, Dienste
- Webpublishing-Assistent, registrieren
- Online-druckstellungs-Assistent, registrieren
- registrieren, Webpublishing-Assistent
- registrieren, Assistent für Online-Druck Bestellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497133d7f0a769fce987745a2341a2e501fe7a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104219407"
---
# <a name="registering-a-service"></a>Registrieren eines Dienstanbieter

Wenn Sie Ihren Dienst der Liste der Anbieter im Webpublishing-Assistenten oder im Assistenten für die Online-druckbestellung hinzufügen möchten, müssen Sie den entsprechenden Schlüssel und seine Werte der Windows-Registrierung hinzufügen.

## <a name="required-keys-and-values"></a>Erforderliche Schlüssel und Werte

Fügen Sie einen Schlüssel hinzu, wie unten gezeigt, um den Dienst der Liste der Anbieter für den Webpublishing-Assistenten hinzuzufügen.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Fügen Sie einen Schlüssel hinzu, wie unten gezeigt, um den Dienst der Liste der Anbieter für den Online-druckstellungs-Assistenten hinzuzufügen.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Jeder Wert ist eine Zeichenfolge vom Typ reg \_ SZ. Stellen Sie die Daten wie in der folgenden Tabelle erläutert bereit. 

| Wertname     | Erklärung                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IconPath       | Der vollständige Pfad zur Symbol Datei, einschließlich des Datei namens.                                                                                                                                                                                                                                                                                                                                                                        |
| DisplayName    | Der Name, der für Ihren Dienst in der Anbieterliste des Assistenten angezeigt wird.                                                                                                                                                                                                                                                                                                                                                             |
| BESCHREIBUNG    | Eine kurze Beschreibung für Ihren Dienst. Diese Beschreibung wird auch in der Anbieterliste des Assistenten direkt unterhalb des Namens Ihres Dienstanbietern angezeigt.                                                                                                                                                                                                                                                                                    |
| HREF           | Die URL der ersten Seite Ihres Dienstanbieter.                                                                                                                                                                                                                                                                                                                                                                                      |
| SupportedTypes | Die von Ihrem Dienst unterstützten Dateitypen. Beispielsweise *\* . jpg*. Wenn Sie nur bestimmte Dateitypen angeben, wird der Dienst nur angezeigt, wenn diese Dateitypen ausgewählt wurden. Wenn mehr als ein Dateityp ausgewählt wurde, wird der Dienst angezeigt, wenn einer dieser Dateitypen von Ihrem Dienst unterstützt wird. Wenn Sie mehrere Dateitypen angeben möchten, trennen Sie diese durch Semikolons in der Liste. Beispiel: *\* . jpg; \* . BMP*. |



 

Im folgenden finden Sie ein umfassendes Beispiel für einen fotoverarbeitungs Dienst mit dem Namen "MyProvider".

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

Wenn die URL des Dienes aufgerufen wird, werden zwei Werte am Ende der URL – LCID und langid hinzugefügt. Beispielsweise könnte die URL-Zeichenfolge für das obige Beispiel https: \/ /www.MyProvider.com/Intro.htm? LCID = 1033&langid = 1033 lauten. Diese Variablen werden für Sprach-und Lokalisierungs Informationen verwendet.

-   **LCID** wird verwendet, um den Server über die Land-/Regions-und Spracheinstellungen des Clients zu informieren. Er wird nicht verwendet, um die Sprache der Benutzeroberfläche des Clients zu bestimmen. er wird jedoch verwendet, um das richtige Format für Währung, Datum und Uhrzeit und andere regionsspezifische Daten zu bestimmen.
-   **LangID** wird verwendet, um den Server über die Standard Spracheinstellung des Clients zu informieren, sodass die richtige Sprache in der Benutzeroberfläche verwendet werden kann.

 

 




