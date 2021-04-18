---
title: Kompilieren des Beispielprojekts
description: Kompilieren des Beispielprojekts
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player Online Stores, Kompilieren von Beispielprojekten
- Online Stores, Kompilieren von Beispielprojekten
- Typ 2 Online Stores, Kompilieren von Beispielprojekten
- Windows Media Player Online Stores, Beispiel Projekte
- Online Stores, Beispiel Projekte
- Typ 2 Online Stores, Beispiel Projekte
- Windows Media Player Online Stores, Projekt-Assistent
- Online Stores, Projekt-Assistent
- Typ 2 Online Stores, Projekt-Assistent
- Plug-ins, Projekt-Assistent
- Windows Media Player-Plug-ins, Projekt-Assistent
- Kompilieren von Beispielprojekten
- Beispiele, Typ 2 Online Stores
- Projekt-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340220"
---
# <a name="compiling-the-sample-project"></a>Kompilieren des Beispielprojekts

Der Assistent generiert alle Dateien, die Sie benötigen, um das Beispiel Projekt zu kompilieren, sodass Sie die standardmäßigen Projekteinstellungen nicht ändern müssen. Klicken Sie in Visual Studio im Menü **Erstellen** auf Projekt Mappe **Erstellen** , um die COM-Komponente zu erstellen und zu registrieren. Standardmäßig ist die Debug-Konfiguration aktiv.

> [!Note]  
> In Windows Vista und höher wird das Projekt nicht erfolgreich erstellt, es sei denn, Sie führen Visual Studio mit einem vollen Administrator Zugriffs Token aus. Klicken Sie mit der rechten Maustaste auf den Namen oder das Symbol von Visual Studio, und klicken Sie auf **als Administrator ausführen**

 

Bevor Sie versuchen, das Projekt zu erstellen, stellen Sie sicher, dass Sie Ihre Entwicklungsumgebung so konfigurieren, dass Sie auf die Ordner include und lib verweist, in denen Sie die Windows SDK installiert haben. Der Compiler und Linker benötigen Zugriff auf einige der Dateien in diesen Ordnern.

Wenn Sie das Visual Studio-Registrierungsprogramm ausgeführt haben, das im Windows Vista SDK enthalten ist, wurde Ihre Entwicklungsumgebung wahrscheinlich bereits so konfiguriert, dass Sie auf die Windows SDK include-und lib-Ordner verweist. Andernfalls müssen Sie Ihre Entwicklungsumgebung manuell konfigurieren.

Führen Sie die folgenden Schritte aus, um Visual Studio manuell zu konfigurieren.

1.  Klicken Sie im Menü **Extras** auf **Optionen**.
2.  Klicken Sie auf **Projekte und Projekt** Mappen und dann auf **VC + +-Verzeichnisse**.
3.  Klicken Sie unter **Verzeichnisse anzeigen für** auf Dateien oder **Bibliotheksdateien** **einschließen** .
4.  Fügen Sie die Verzeichnisse für die erforderlichen Dateien hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln des Plug-Ins für einen Typ 2-Online Store](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




