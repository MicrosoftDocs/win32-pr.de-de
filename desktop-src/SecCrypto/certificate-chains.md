---
description: Um Zertifikate für die Sicherheit zu verwenden, müssen die Authentizität und die Gültigkeit der einzelnen empfangenen Zertifikate überprüft werden. Diese Überprüfung hängt von dem Vertrauens Konzept und der Delegierung von Trust \[ Platform Software Development Kit (SDK) ab \] .
ms.assetid: e6cb0280-f531-40dc-bbb1-d8115d026e03
title: Zertifikat Ketten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea42b6788997a86aade6f89d0f35d92a74daafc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484691"
---
# <a name="certificate-chains"></a>Zertifikat Ketten

Um Zertifikate für die Sicherheit zu verwenden, müssen die Authentizität und die Gültigkeit der einzelnen empfangenen [*Zertifikate*](../secgloss/c-gly.md) überprüft werden. Diese Überprüfung hängt von dem Vertrauens Konzept und der Delegierung der Vertrauensstellung ab. Weitere Informationen finden Sie unter [Hierarchie der Vertrauens](hierarchy-of-trust.md)Stellung.

Jedes Zertifikat enthält ein Betreff-Feld, das die Einzelperson oder Gruppe identifiziert, für die das Zertifikat ausgestellt wurde. Jedes Zertifikat enthält auch ein Aussteller Feld, mit dem die Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) identifiziert wird, die zur Zertifizierung der Identität des Subjekts autorisiert ist.

Eine Zertifikat Kette besteht aus allen Zertifikaten, die zum zertifizieren des Antragstellers erforderlich sind, der durch das Endzertifikat identifiziert wird. In der Praxis umfasst dies das Endzertifikat, die Zertifikate von zwischen Zertifizierungsstellen und das Zertifikat einer Stamm Zertifizierungsstelle, die von allen Parteien in der Kette als vertrauenswürdig eingestuft wird. Jede zwischen Zertifizierungsstelle in der Kette enthält ein Zertifikat, das von der Zertifizierungsstelle eine Ebene oberhalb der Zertifizierungsstelle in der Vertrauens Hierarchie ausgestellt wurde. Die Stamm Zertifizierungsstelle gibt ein Zertifikat für sich selbst aus.

Bei der Überprüfung der Authentizität und Gültigkeit eines neu empfangenen Zertifikats werden alle Zertifikate in der Zertifikatskette der ursprünglichen, universell vertrauenswürdigen Zertifizierungsstelle über alle zwischen Zertifizierungsstellen überprüft, bis das soeben empfangene Zertifikat, das als Endzertifikat bezeichnet wird, überprüft wird. Ein neues Zertifikat kann nur dann als vertrauenswürdig eingestuft werden, wenn jedes Zertifikat in der Kette des Zertifikats ordnungsgemäß ausgestellt und gültig ist.

Das Nachverfolgen aller Zertifikate, die ein neues Endzertifikat zurückgibt, kann mühsam werden. Aus diesem Grund bietet die [*CryptoAPI*](../secgloss/c-gly.md) 2,0-Technologiefunktionen, die das Erstellen der Zertifikatskette automatisieren, die ein bestimmtes Endzertifikat zurückgibt. Diese Funktionen überprüfen auch die Gültigkeit der einzelnen Zertifikate in einer Kette und melden Sie.

Bei den Ketten Erstellungs-und Überprüfungs Funktionen von [*CryptoAPI*](../secgloss/c-gly.md) 2,0 wird eine Kette von Zertifikaten erstellt und überprüft. Eine Kette-Engine definiert einen Store-Namespace und eine Cache Partitionierung für die Zertifikat Verkettungs Infrastruktur. CryptoAPI 2.0 stellt eine Standard Kette-Engine für jeden Anwendungsprozess bereit, der nur Standardsystem Speicher (z. b. my, root, ca und Trust) für die Ketten Bildung und-Zwischenspeicherung verwendet. Eine Anwendung kann einen eigenen Speicher Namespace definieren oder über einen eigenen partitionierten Cache verfügen, indem eine eigene Kette-Engine erstellt wird. Um ein optimales zwischen Speicherungs Verhalten zu erzielen, empfiehlt es sich, beim Starten der Anwendung ein einzelnes Ketten Modul zu erstellen und dieses Ketten Modul während der gesamten Lebensdauer der Anwendung zu verwenden.

Eine Liste der Funktionen finden Sie unter Funktionen für die über [Prüfung der Zertifikat Kette](cryptography-functions.md). Ein Programm, das Zertifikat Ketten erstellt und Zertifikate überprüft, finden Sie unter [Beispiel C-Programm: Erstellen einer Zertifikat Kette](example-c-program-creating-a-certificate-chain.md).

 

 
