---
description: Aus Sicherheitsgründen sind sichere Transformationen manchmal notwendig.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Gesicherte Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e498d6049a2c913ca78f12b6a8700a104af37c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869040"
---
# <a name="secured-transforms"></a>Gesicherte Transformationen

Aus Sicherheitsgründen sind sichere Transformationen manchmal notwendig. Gesicherte Transformationen werden lokal auf dem Computer des Benutzers an einem Speicherort gespeichert, an dem der Benutzer auf einem sicheren Dateisystem keinen Schreibzugriff hat. Solche Transformationen werden an diesem Speicherort während der Installation oder Ankündigung des Pakets zwischengespeichert. Nur Administratoren und das lokale System verfügen über Schreibzugriff auf diesen Speicherort. Ein Benutzer ohne Administratorrechte kann die Transformations Datei nicht ändern. Bei einer nachfolgenden [Installation](installation-on-demand.md) oder [Wartung](maintenance-installation.md) des Pakets verwendet das Installationsprogramm die zwischengespeicherten Transformationen.

Legen Sie zum Angeben von sicherem Transformations Speicher die [transformssecure-Richtlinie](transformssecure-policy.md)fest, legen Sie die [**transformssecure**](transformssecure.md) -Eigenschaft fest, oder übergeben Sie das Symbol @ oder \| in der Liste Transformationen. Beachten Sie, dass Sie keine gesicherten und ungesicherten Transformationen in dieselbe Transformations Liste einschließen können. Siehe [Anwenden von Transformationen](applying-transforms.md).

Durch das Entfernen des Produkts durch einen beliebigen Benutzer werden alle gesicherten Transformationen für das Produkt auf dem Computer des Benutzers entfernt.

Wenn das Installationsprogramm feststellt, dass eine gesicherte Transformation nicht lokal verfügbar ist, wird versucht, den Transformations Cache aus einer Quelle wiederherzustellen. Sichere Transformationen können eine sichere Quelle oder ein sicherer vollständiger Pfad sein:

-   Aus dem lokalen Transformations Cache fehlende [Secure-at-Source-Transformationen](secure-at-source-transforms.md) werden aus dem Stamm der Quelle der MSI-Datei wieder hergestellt.
-   [Sichere vollständige Pfad Transformationen](secure-full-path-transforms.md) , die im lokalen Transformations Cache fehlen, werden vom ursprünglichen vollständigen Pfad wieder hergestellt, der durch die Liste der Transformationen angegeben wird.

 

 



