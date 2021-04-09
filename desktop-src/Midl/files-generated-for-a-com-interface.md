---
title: Für eine COM-Schnittstelle generierte Dateien
description: Für COM-Schnittstellen kombiniert der Mittelwert Compiler alle Client-und Objekt Server-Erweiterungs Routinen und-Daten in einer einzelnen Schnittstellen Proxy Datei.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- Mittel l compilermittell, Mittel l und com
- COM-Mittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948665"
---
# <a name="files-generated-for-a-com-interface"></a>Für eine COM-Schnittstelle generierte Dateien

Für COM-Schnittstellen kombiniert der Mittelwert Compiler alle Client-und Objekt Server-Erweiterungs Routinen und-Daten in einer einzelnen Schnittstellen Proxy Datei. Diese Datei enthält die Ersatz Einstiegspunkte für Clients und Server. Außerdem generiert der-compilercompiler eine Schnittstellen Header Datei, eine Schnittstellen-UUID-Datei und eine Schnittstellen Registrierungsdatei. Diese Dateien werden beim Erstellen einer Proxy-dll verwendet, die den Code enthält, um die Verwendung der-Schnittstelle sowohl von Client Anwendungen als auch von Objekt Servern zu unterstützen. Beim Erstellen der ausführbaren Datei für eine Client Anwendung, die die-Schnittstelle verwendet, verwenden Sie außerdem die-Schnittstellen Header Datei und die-Schnittstellen-UUID-Datei.

In den folgenden Themen werden die einzelnen Dateien beschrieben, die für eine benutzerdefinierte COM-Schnittstelle generiert werden, indem Sie das **\[** [**Object**](object.md) - **\]** Attribut in die Schnittstellen Attribut Liste der IDL-Datei einschließen:

-   [Die Schnittstellen Proxy Datei](the-interface-proxy-file.md)
-   [Die Header Dateien](the-header-files.md)
-   [Die UUID-Schnittstellen Datei](the-interface-uuid-file.md)
-   [Die Schnittstellen Registrierungsdatei](the-interface-registration-file.md)

Weitere Informationen finden Sie unter [Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md), [**/App \_ config**](-app-config.md), [Interface Definition (IDL)-Datei](interface-definition-idl-file.md)und entwickeln [und Registrieren einer Proxy-dll](../com/building-and-registering-a-proxy-dll.md).

 

 