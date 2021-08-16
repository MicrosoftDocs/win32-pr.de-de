---
description: Um Zertifikate aus Sicherheitsgründen zu verwenden, müssen die Authentizität und Gültigkeit jedes empfangenen Zertifikats überprüft werden. Diese Überprüfung hängt vom Konzept der Vertrauensstellung und der Delegierung des \[ Trusts Platform Software Development Kit (SDK) \] ab.
ms.assetid: e6cb0280-f531-40dc-bbb1-d8115d026e03
title: Zertifikatketten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6efdd49cbd66c74805cc560286e5f15a981ef200df5523c602c2bb4b395a04e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771939"
---
# <a name="certificate-chains"></a>Zertifikatketten

Um [*Zertifikate*](../secgloss/c-gly.md) aus Sicherheitsgründen zu verwenden, müssen die Authentizität und Gültigkeit jedes empfangenen Zertifikats überprüft werden. Diese Überprüfung hängt vom Konzept der Vertrauensstellung und der Delegierung von Vertrauensstellungen ab. Weitere Informationen finden Sie unter [Hierarchie der Vertrauensstellung.](hierarchy-of-trust.md)

Jedes Zertifikat enthält ein Betrefffeld, das die Person oder Gruppe identifiziert, für die das Zertifikat ausgestellt wurde. Jedes Zertifikat enthält auch ein Ausstellerfeld, das die [*Zertifizierungsstelle*](../secgloss/c-gly.md) identifiziert, die berechtigt ist, die Identität des Antragstellers zu zertifizieren.

Eine Zertifikatkette besteht aus allen Zertifikaten, die zum Zertifizieren des vom Endzertifikat identifizierten Antragstellers erforderlich sind. In der Praxis umfasst dies das Endzertifikat, die Zertifikate von Zwischenzertifizierungsstellen und das Zertifikat einer Stammzertifizierungsstelle, die von allen Parteien in der Kette als vertrauenswürdig eingestuft wird. Jede Zwischenzertifizierungsstelle in der Kette enthält ein Zertifikat, das von der Zertifizierungsstelle eine Ebene darüber in der Vertrauenshierarchie ausgestellt wurde. Die Stammzertifizierungsstelle stellt ein Zertifikat für sich selbst aus.

Der Prozess der Überprüfung der Authentizität und Gültigkeit eines neu empfangenen Zertifikats umfasst die Überprüfung aller Zertifikate in der Zertifikatkette von der ursprünglichen, universell vertrauenswürdigen Zertifizierungsstelle über alle Zwischenzertifizierungsstellen bis hin zu dem gerade empfangenen Zertifikat, das als Endzertifikat bezeichnet wird. Ein neues Zertifikat kann nur dann als vertrauenswürdig eingestuft werden, wenn jedes Zertifikat in der Kette dieses Zertifikats ordnungsgemäß ausgestellt und gültig ist.

Die Nachverfolgung aller Zertifikate, die ein neues Endzertifikat sichern, kann umständlich werden. Daher stellt [*die CryptoAPI*](../secgloss/c-gly.md) 2.0-Technologie Funktionen bereit, die die Erstellung der Zertifikatkette automatisieren, die ein bestimmtes Endzertifikat unterstützt. Diese Funktionen überprüfen und melden auch die Gültigkeit jedes Zertifikats in einer Kette.

Die Funktionen zum Erstellen und Überprüfen von Ketten von [*CryptoAPI*](../secgloss/c-gly.md) 2.0 verwenden eine Ketten-Engine, um Zertifikatketten zu erstellen und zu überprüfen. Eine Ketten-Engine definiert einen Speichernamespace und eine Cachepartitionierung für die Zertifikatsketteninfrastruktur. CryptoAPI 2.0 stellt eine Standardketten-Engine für jeden Anwendungsprozess bereit, der nur Standardsystemspeicher (z. B. MY, Root, CA und Trust) zum Erstellen und Zwischenspeichern von Ketten verwendet. Eine Anwendung kann ihren eigenen Speichernamespace definieren oder über einen eigenen partitionierten Cache verfügen, indem sie eine eigene Ketten-Engine erstellt. Um ein optimales Cacheverhalten zu erzielen, empfehlen wir Ihnen, beim Anwendungsstart eine einzelne Ketten-Engine zu erstellen und diese Ketten-Engine während der gesamten Lebensdauer der Anwendung zu verwenden.

Eine Liste der Funktionen finden Sie unter [Certificate Chain Verification Functions](cryptography-functions.md). Ein Programm, das Zertifikatketten erstellt und Zertifikate überprüft, finden Sie unter [C-Beispielprogramm: Erstellen einer Zertifikatkette.](example-c-program-creating-a-certificate-chain.md)

 

 
