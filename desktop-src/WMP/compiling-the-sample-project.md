---
title: Kompilieren der Project
description: Kompilieren der Project
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player,Kompilieren von Beispielprojekten
- Onlineshops,Kompilieren von Beispielprojekten
- 'Typ 2: Onlineshops,Kompilieren von Beispielprojekten'
- Windows Media Player,Beispielprojekte
- Onlineshops,Beispielprojekte
- 'Typ 2: Onlineshops,Beispielprojekte'
- Windows Media Player,Projekt-Assistent
- Onlineshops,Projekt-Assistent
- Typ 2 Onlineshops,Projekt-Assistent
- Plug-Ins, Projekt-Assistent
- Windows Media Player-Plug-Ins,Projekt-Assistent
- Kompilieren von Beispielprojekten
- Beispiele,Geben Sie 2 Onlineshops ein.
- Projekt-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55b2f5a4b6d29b227b08654cfcde2a89cc97b224fc756251ae9554f029f22416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763940"
---
# <a name="compiling-the-sample-project"></a>Kompilieren der Project

Der Assistent generiert alle Dateien, die Sie zum Kompilieren des Beispielprojekts benötigen, sodass Sie die Standardprojekteinstellungen nicht ändern müssen. Klicken Visual Studio im Menü **Erstellen** auf  Projektmappe erstellen, um die COM-Komponente zu erstellen und zu registrieren. Standardmäßig ist die Debugkonfiguration aktiv.

> [!Note]  
> In Windows Vista und höher wird das Projekt nur erfolgreich erstellt, wenn Sie Visual Studio mit einem vollständigen Administratorzugriffstoken ausführen. Klicken Sie mit der rechten Maustaste Visual Studio Namen oder Symbol, und klicken Sie **auf Als Administrator ausführen.**

 

Bevor Sie versuchen, das Projekt zu erstellen, müssen Sie Ihre Entwicklungsumgebung so konfigurieren, dass sie auf die Ordner Include und Lib verweisen, in denen Sie das Windows INSTALLIERT haben. Ihr Compiler und Linker benötigen Zugriff auf einige der Dateien in diesen Ordnern.

Wenn Sie das Visual Studio Registration-Hilfsprogramm im Windows Vista SDK ausführen, wurde Ihre Entwicklungsumgebung wahrscheinlich bereits so konfiguriert, dass sie auf die Include- und Lib-Ordner des Windows SDK verweisen kann. Andernfalls müssen Sie Ihre Entwicklungsumgebung manuell konfigurieren.

Um die Visual Studio manuell zu konfigurieren, verwenden Sie die folgenden Schritte.

1.  Klicken Sie im Menü **Extras** auf **Optionen**.
2.  Klicken **Sie auf Projekte und Projekt** projektiert , und klicken Sie dann VC++ Verzeichnisse **.**
3.  Klicken **Sie unter Verzeichnisse für anzeigen** auf Dateien **oder** **Bibliotheksdateien enthalten.**
4.  Fügen Sie die Verzeichnisse für die erforderlichen Dateien hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen des Plug-Ins für eine Online-Store](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




