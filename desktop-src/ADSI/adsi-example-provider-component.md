---
title: ADSI-Beispielanbieterkomponente
description: Anbieterautoren von Active Directory-Dienstanbietern finden diesen Abschnitt von besonderem Interesse, da er die ADSI-Beispielanbieterkomponente ausführlich beschreibt.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f1ff1d998a9db620c6dc6fb4402f126f556c95a45d589410800ea9c4b335a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023898"
---
# <a name="adsi-example-provider-component"></a>ADSI-Beispielanbieterkomponente

Anbieterautoren von Active Directory-Dienstanbietern finden diesen Abschnitt von besonderem Interesse, da er die ADSI-Beispielanbieterkomponente ausführlich beschreibt. ADSI-Anbieterautoren können den Beispielanbieter installieren und das Codeframework als Grundlage verwenden, um ihre eigene Implementierung zu erstellen. Die folgenden Themen werden erörtert:

[Unter Installieren der Beispielanbieterkomponente](installing-the-example-provider-component.md) wird beschrieben, wie sie den ADSI-Beispielanbieter und dessen Modellverzeichnis installieren. Dieser Abschnitt enthält eine Liste der Registrierungseinstellungen.

[Die Verzeichnisdefinition](directory-definition.md) beschreibt die Verzeichniseinträge, die von der Beispielanbieterkomponente definiert werden.

[Die Schemaverwaltung](schema-management.md) beschreibt, wie jedes Element im Verzeichnisdienst der Beispielanbieterkomponente durch einen bestimmten Active Directory-Objekttyp dargestellt werden kann.

Beim Binden an ein [Active Directory-Objekt](binding-to-an-active-directory-object.md) wird beschrieben, wie die Beispielanbieterkomponente bei einer ADsPath-Zeichenfolge dieses Element identifiziert, den entsprechenden Active Directory-Objekttyp dafür erstellt und den angeforderten Typ des Schnittstellenzeigers für dieses Objekt abruft, um es an die ADs-Clientsoftware zurückübergibt.

[Enumeratorobjekte](enumerator-objects.md) listet die spezifischen Typen von Enumerationen auf, die von der Beispielanbieterkomponente bereitgestellt werden, und in welchem Quellcode sich die Implementierungen finden.

[Die Codeübersicht](code-overview.md) enthält eine Beschreibung der einzelnen Teile der Beispielanbieterkomponente auf Aufgabenebene.

[Codedetails](code-details.md) listet die Softwaremodule und deren Inhalt auf.

 

 




