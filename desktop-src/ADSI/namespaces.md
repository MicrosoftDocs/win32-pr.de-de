---
title: Namespaces
description: Objekte, die sich in einem bestimmten Namespace befinden, werden durch einen eindeutigen Namen identifiziert.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- Namespaces ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387958"
---
# <a name="namespaces"></a>Namespaces

Objekte, die sich in einem bestimmten Namespace befinden, werden durch einen eindeutigen Namen identifiziert. Beispielsweise befinden sich auf einem PC-Laufwerk gespeicherte Dateien im Dateisystem-Namespace. Der eindeutige Name einer Datei basiert darauf, wo Sie im Dateisystem-Namespace gespeichert wird. Beispiel:


```C++
C:\public\documents\adsi\adsi_spec.doc
```



Verzeichnisdienst-Namespaces identifizieren auch die Objekte, die Sie mit eindeutigen Namen enthalten, die normalerweise auf dem Speicherort im Verzeichnis basieren, an dem das Objekt gefunden werden kann. Beispielsweise kann ein bestimmtes Objekt in einem X. 500-Verzeichnis einen Namen wie den folgenden aufweisen:


```C++
CN=John,OU=Marketing,O=Fabrikam
```



Verschiedene Verzeichnisdienste verwenden verschiedene Formulare, um die darin enthaltenen Objekte zu benennen. Dies vereinfacht den Umgang mit verschiedenen Namespaces, insbesondere für Entwickler, die alle unterschiedlichen Umgebungen in Betracht ziehen, in denen der Code möglicherweise ausgeführt wird.

Ein Ziel von Active Directory Service Interfaces (ADSI) ist die Bereitstellung eines Benennungs Frameworks, das den Zugriff auf Namespaces verschiedener Verzeichnis Dienstanbieter ermöglicht.

ADSI definiert eine Benennungs Konvention, mit der ein Objekt in einer heterogenen Umgebung eindeutig identifiziert werden kann. Diese Namen werden als ADsPath-Zeichen folgen bezeichnet. ADsPath-Zeichen folgen benötigen verschiedene Formen:


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



Es können zusätzliche zusätzliche Formate von ADSI-Anbietern eingeführt werden (z. b. der ADSI-Anbieter für den Internetinformationsdienste-Server, der die adspaths "IIS://" unterstützt).

 

 




