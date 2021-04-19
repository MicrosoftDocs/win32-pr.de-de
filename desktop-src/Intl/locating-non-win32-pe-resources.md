---
description: Suchen von nicht-Win32 PE-Ressourcen
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Suchen von nicht-Win32 PE-Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079288cd6200eb64289f474636cbc8dc046c1e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356830"
---
# <a name="locating-non-win32-pe-resources"></a>Suchen von nicht-Win32 PE-Ressourcen

Um nicht-Win32 PE-Ressourcen zu suchen, sollte Ihre Anwendung zuerst die [**getfilemuipath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) -Funktion aufrufen, um die sprachspezifische Ressourcen Datei zu suchen, aus der Ressourcen geladen werden. Wenn die Anwendung den Einstellungen der Systemsprache folgt, muss Sie die-Funktion mit den für " \_ \_ \| \_ \_ \_ \_ *dwFlags* " angegebenen benutzerdefinierten UI-Sprachen für  "MUI Language Name MUI" und "Null" für " *pwszlanguage*" aufruft. Wenn die Anwendung anwendungsspezifische Spracheinstellungen verwendet, wird **getfilemuipath** verwendet, um zu bestimmen, ob eine sprachspezifische Datei vorhanden ist, indem die Sprache im *pwszlanguage* -Parameter angegeben wird.

Nach dem Aufrufen von [**getfilemuipath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)muss die Anwendung benutzerdefinierte Funktionen definieren, um das Ressourcen Modul zu laden und bestimmte Ressourcen daraus zu laden. Wenn Sie z. b. eine txt-oder XML-Ressourcen Datei verwenden, muss die Anwendung einen txt-oder XML-Parser verwenden, um die Datei zu laden und dann den Inhalt der Datei für jede erforderliche Ressource zu analysieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der mehrsprachigen Benutzeroberfläche](using-multilingual-user-interface.md)
</dt> <dt>

[**Getfilemuipath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



