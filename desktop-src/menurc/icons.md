---
title: Symbole (Menüs und andere Ressourcen)
description: In diesem Abschnitt werden Symbole erläutert, bei denen es sich um Bitmap-Bilder in Kombination mit einer Maske handelt, um transparente Bereiche im Bild
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\icons.htm
keywords:
- Ressourcen, Symbole
- Symbole, Info
- RT_ICON-Ressource
- RT_GROUP_ICON-Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c96e740c23bb61cfdaa6cfbcbf6d0ce7538586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391457"
---
# <a name="icons-menus-and-other-resources"></a>Symbole (Menüs und andere Ressourcen)

Ein *Symbol* ist ein Bild, das aus einem Bitmap-Bild kombiniert mit einer Maske besteht, um transparente Bereiche im Bild zu erstellen. Der Begriff "Symbol" kann auf eine der folgenden Optionen verweisen:

-   Ein einzelnes Symbolbild. Dies ist eine Ressource vom Typ **RT- \_ Symbol**.
-   Eine Gruppe von Images, von der das System oder eine Anwendung das geeignetste Symbol basierend auf Größe und Farbtiefe auswählen kann. Dies ist eine Ressource vom Typ **RT- \_ Gruppen \_ Symbol**.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                 | BESCHREIBUNG                                                 |
|--------------------------------------|-------------------------------------------------------------|
| [Informationen zu Symbolen](about-icons.md)       | Erläutert Symbole.<br/>                                 |
| [Verwenden von Symbolen](using-icons.md)       | Erläutert das Ausführen von Aufgaben im Zusammenhang mit Symbolen.<br/> |
| [Symbol Verweis](icon-reference.md) | Enthält die API-Referenz.<br/>                      |



 

### <a name="icon-functions"></a>Symbol Funktionen



| Name                                                               | BESCHREIBUNG                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Copyicon**](/windows/desktop/api/Winuser/nf-winuser-copyicon)                                       | Kopiert das angegebene Symbol von einem anderen Modul in das aktuelle Modul. <br/>                                                                                                                                      |
| [**"Kreateicon"**](/windows/desktop/api/Winuser/nf-winuser-createicon)                                   | Erstellt ein Symbol mit der angegebenen Größe, den angegebenen Farben und den angegebenen Bitmustern. <br/>                                                                                                                                    |
| [**"Kreateiconfiguration"**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource)           | Erstellt ein Symbol oder einen Cursor aus Ressourcen Bits, die das Symbol beschreiben.<br/>                                                                                                                                          |
| [**"Kreateizufromresourceex"**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex)       | Erstellt ein Symbol oder einen Cursor aus Ressourcen Bits, die das Symbol beschreiben. <br/>                                                                                                                                         |
| [**"Kreatei\indirekt"**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)                   | Erstellt ein Symbol oder einen Cursor aus einer [**iconinfo**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) -Struktur. <br/>                                                                                                                                 |
| [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                 | Zerstört ein Symbol und gibt den Arbeitsspeicher frei, den das Symbol belegt hat. <br/>                                                                                                                                                  |
| [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)                                       | Zeichnet ein Symbol oder einen Cursor in den angegebenen Gerätekontext.<br/>                                                                                                                                                 |
| [**Drawiconfiguration**](/windows/desktop/api/Winuser/nf-winuser-drawiconex)                                   | Zeichnet ein Symbol oder einen Cursor in den angegebenen Gerätekontext, wobei die angegebenen Raster Vorgänge ausgeführt werden und das Symbol oder der Cursor wie angegeben gestreckt oder komprimiert wird. <br/>                                     |
| [**Duplialisieicon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon)                             | Erstellt ein Duplikat eines angegebenen Symbols.<br/>                                                                                                                                                                   |
| [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona)             | Ruft ein Handle zu einem indizierten Symbol ab, das in einer Datei gefunden wurde, oder ein Symbol in einer zugeordneten ausführbaren Datei. <br/>                                                                                                  |
| [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona)                                 | Ruft ein Handle für ein Symbol aus der angegebenen ausführbaren Datei, dll oder Symbol Datei ab.<br/>                                                                                                                        |
| [**Extracticonfiguration**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)                             | Erstellt ein Array von Handles für große oder kleine Symbole, die aus der angegebenen ausführbaren Datei, dll oder Symbol Datei extrahiert werden. <br/>                                                                                      |
| [**Getiverbindunginfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo)                                 | Ruft Informationen zum angegebenen Symbol oder Cursor ab. <br/>                                                                                                                                                 |
| [**Getimitinfoex**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa)                             | Ruft Informationen zum angegebenen Symbol oder Cursor ab. [**Getideinfoex**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa) erweitert [**getidininfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) mithilfe der neueren [**iconinfoex**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa) -Struktur.<br/> |
| [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                                       | Lädt die angegebene Symbol Ressource aus der ausführbaren Datei (. exe), die einer Anwendungs Instanz zugeordnet ist.<br/>                                                                                                 |
| [**Lookupi\idfromdirectory**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectory)     | Durchsucht Symbol-oder Cursor Daten nach dem Symbol oder Cursor, das am besten zum aktuellen Anzeigegerät passt.<br/>                                                                                                     |
| [**Lookupienidfromdirectorienex**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) | Durchsucht Symbol-oder Cursor Daten nach dem Symbol oder Cursor, das am besten zum aktuellen Anzeigegerät passt. <br/>                                                                                                    |
| [**Privateextracticons**](/windows/desktop/api/Winuser/nf-winuser-privateextracticonsa)                 | Erstellt ein Array von Handles für Symbole, die aus einer angegebenen Datei extrahiert werden.<br/>                                                                                                                             |



 

### <a name="icon-structures"></a>Symbol Strukturen



| Name                               | BESCHREIBUNG                                                                                                                                                                                                                                     |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iconinfo**](/windows/desktop/api/Winuser/ns-winuser-iconinfo)       | Enthält Informationen über ein Symbol oder einen Cursor. <br/>                                                                                                                                                                                     |
| [**Iconinfoex**](/windows/desktop/api/Winuser/ns-winuser-iconinfoexa)   | Enthält Informationen über ein Symbol oder einen Cursor. Erweitert [**iconinfo**](/windows/desktop/api/Winuser/ns-winuser-iconinfo). Wird von [**geticonfig INFOEX**](/windows/desktop/api/Winuser/nf-winuser-geticoninfoexa)verwendet.<br/>                                                                                                |
| [**Iconmetrics**](/windows/win32/api/winuser/ns-winuser-iconmetricsa) | Enthält die den Symbolen zugeordneten skalierbaren Metriken. Diese Struktur wird zusammen mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion verwendet, wenn die **SPI- \_ getien-** oder SPI-Aktivität "abtienconfiguration" angegeben wird. **\_**<br/> |



 

 

