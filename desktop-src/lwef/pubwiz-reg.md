---
title: Registrieren eines Diensts
description: Um Ihren Dienst der Liste der Anbieter im Webveröffentlichungs-Assistenten oder im Onlinedruckreihenfolge-Assistenten hinzuzufügen, müssen Sie der Windows Registrierung den entsprechenden Schlüssel und dessen Werte hinzufügen.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- register,services
- Webveröffentlichungs-Assistent,Registrieren
- Onlinedruckreihenfolge-Assistent,Registrieren
- Register, Webveröffentlichungs-Assistent
- register,Online Print Ordering Wizard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f5e3f43fe981558fcbf8573eb8768646f112f4816486159cc7c16d71e40e5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608640"
---
# <a name="registering-a-service"></a>Registrieren eines Diensts

Um Ihren Dienst der Liste der Anbieter im Webveröffentlichungs-Assistenten oder im Onlinedruckreihenfolge-Assistenten hinzuzufügen, müssen Sie der Windows Registrierung den entsprechenden Schlüssel und dessen Werte hinzufügen.

## <a name="required-keys-and-values"></a>Erforderliche Schlüssel und Werte

Um Ihren Dienst der Liste der Anbieter für den Webveröffentlichungs-Assistenten hinzuzufügen, fügen Sie wie unten gezeigt einen Schlüssel hinzu.

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

Um Ihren Dienst der Liste der Anbieter für den Onlinedruckbestellungs-Assistenten hinzuzufügen, fügen Sie wie unten gezeigt einen Schlüssel hinzu.

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

Jeder der Werte ist eine Zeichenfolge vom Typ REG \_ SZ. Geben Sie die Daten wie in der folgenden Tabelle beschrieben an. 

| Wertname     | Erklärung                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IconPath       | Der vollständige Pfad zur Symboldatei, einschließlich des Dateinamens.                                                                                                                                                                                                                                                                                                                                                                        |
| DisplayName    | Der Name, der für Ihren Dienst in der Anbieterliste des Assistenten angezeigt wird.                                                                                                                                                                                                                                                                                                                                                             |
| Beschreibung    | Eine kurze Beschreibung für Ihren Dienst. Diese Beschreibung wird auch in der Anbieterliste des Assistenten direkt unter dem Namen Ihres Diensts angezeigt.                                                                                                                                                                                                                                                                                    |
| Href           | Die URL der ersten Seite Ihres Diensts.                                                                                                                                                                                                                                                                                                                                                                                      |
| SupportedTypes | Die von Ihrem Dienst unterstützten Dateitypen. Beispiel: *\*.jpg*. Wenn Sie nur bestimmte Dateitypen angeben, wird Ihr Dienst nur angezeigt, wenn diese Dateitypen ausgewählt wurden. Wenn mehr als ein Dateityp ausgewählt wurde, wird Ihr Dienst angezeigt, wenn einer dieser Dateitypen von Ihrem Dienst unterstützt wird. Wenn Sie mehrere Dateitypen angeben möchten, trennen Sie sie in der Liste durch Semikolons. Beispiel: *\*.jpg; \*.bmp*. |



 

Im Folgenden finden Sie ein vollständiges Beispiel für einen Fotoverarbeitungsdienst mit dem Namen "MyProvider".

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

Wenn die URL Ihres Diensts aufgerufen wird, werden am Ende der URL zwei Werte hinzugefügt: lcid und langid. Die URL-Zeichenfolge für das obige Beispiel kann beispielsweise https: \/ /www.MyProvider.com/Intro.htm?lcid=1033&langid=1033 sein. Diese Variablen werden für Sprach- und Lokalisierungsinformationen verwendet.

-   **lcid** wird verwendet, um den Server über das Land/die Region und die Spracheinstellungen des Clients zu informieren. Sie wird nicht verwendet, um die Sprache der Benutzeroberfläche des Clients zu bestimmen, sondern wird verwendet, um das richtige Format für Währung, Datum und Uhrzeit sowie andere regionsspezifische Daten zu bestimmen.
-   **langid** wird verwendet, um den Server über die Standardspracheinstellung des Clients zu informieren, sodass er die richtige Sprache auf der Benutzeroberfläche verwenden kann.

 

 




