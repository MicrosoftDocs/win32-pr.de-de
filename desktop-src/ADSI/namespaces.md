---
title: Namespaces
description: Objekte, die sich in einem bestimmten Namespace befinden, werden durch einen eindeutigen Namen identifiziert.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- Namespaces ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d416782f2a96ca716f6e803ad9d0b4200c82cff6ad0ad033751a89a5d2c8af1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839381"
---
# <a name="namespaces"></a>Namespaces

Objekte, die sich in einem bestimmten Namespace befinden, werden durch einen eindeutigen Namen identifiziert. Dateien, die auf einem PC-Laufwerk gespeichert sind, befinden sich beispielsweise im Dateisystemnamespace. Der eindeutige Name einer Datei basiert darauf, wo sie im Dateisystemnamespace gespeichert ist. Beispiel:


```C++
C:\public\documents\adsi\adsi_spec.doc
```



Verzeichnisdienstnamespaces identifizieren auch die darin enthaltenen Objekte anhand eindeutiger Namen, die in der Regel auf dem Speicherort im Verzeichnis basieren, in dem das Objekt gefunden werden kann. Beispielsweise kann ein bestimmtes Objekt in einem X.500-Verzeichnis einen Namen wie den folgenden haben:


```C++
CN=John,OU=Marketing,O=Fabrikam
```



Verschiedene Verzeichnisdienste verwenden unterschiedliche Formen, um die darin enthaltenen Objekte zu benennen. Dies erschwert den Umgang mit verschiedenen Namespaces, insbesondere für Entwickler, und berücksichtigt dabei alle unterschiedlichen Umgebungen, in denen der Code ausgeführt werden kann.

Ein Ziel von Active Directory-Dienstschnittstellen (ACTIVE Directory Service Interfaces, ADSI) ist die Bereitstellung eines Benennungsframeworks, das den Zugriff auf Namespaces verschiedener Verzeichnisdienstanbieter ermöglicht.

ADSI definiert eine Namenskonvention, die ein Objekt in einer heterogenen Umgebung eindeutig identifizieren kann. Diese Namen werden als ADsPath-Zeichenfolgen bezeichnet. ADsPath-Zeichenfolgen haben mehrere Formen:


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



Zusätzliche ADsPath-Formate können von verschiedenen ADSI-Anbietern eingeführt werden (z. B. dem ADSI-Anbieter für den Internetinformationsdienste-Server, der die "IIS://" ADsPaths unterstützt).

 

 




