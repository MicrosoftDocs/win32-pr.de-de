---
description: Auf jedem System ist eine begrenzte Anzahl von privaten Datenobjekten für das Speichern von Informationen in einer geschützten, verschlüsselten Weise verfügbar.
ms.assetid: 927473d7-b5bc-4b6f-b303-8a0f8680731d
title: Privates Datenobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccacd1334c9859495acf89075b77a0f10af4cb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128777"
---
# <a name="private-data-object"></a>Privates Datenobjekt

Auf jedem System ist eine begrenzte Anzahl von privaten Datenobjekten für das Speichern von Informationen in einer geschützten, verschlüsselten Weise verfügbar.

Private Datenobjekte werden hauptsächlich zur Unterstützung der Speicherung von Server Konto Kennwörtern bereitgestellt. Dies ist nützlich für Server, die in einem bestimmten Konto ausgeführt werden. Das Kennwort des Server Kontos ist private Daten, die gesichert werden sollen, aber zum Protokollieren des Servers erforderlich sind.

Private Datenobjekte können universell sein, oder es kann sich um einen von drei spezialisierten Typen handeln: lokal, Global und Computer.

Lokale private Datenobjekte können nur lokal von dem Computer gelesen werden, auf dem das Objekt gespeichert ist. Der Versuch, diese Remote zu lesen, führt zu einem Fehler beim Status " \_ Zugriff \_ verweigert". Lokale private Datenobjekte haben Schlüsselnamen, die mit dem Präfix "L $" beginnen. Zusätzlich zu den von Ihnen erstellten lokalen privaten Objekten definiert das Betriebssystem die folgenden lokalen privaten Objekte: $Machine. ACC, SAC, Sai und sansc.

Globale private Datenobjekte sind Global, wenn Sie auf einem Domänen Controller erstellt werden, werden Sie automatisch auf allen Domänen Controllern in dieser Domäne repliziert. Dies bedeutet, dass jeder Domänen Controller in dieser Domäne Zugriff auf die Werte hat, die das globale private Datenobjekt enthält. Im Gegensatz dazu werden globale private Datenobjekte, die auf einem System erstellt werden, das kein Domänen Controller ist, sowie nicht globale private Datenobjekte nicht repliziert. Globale private Datenobjekte haben Schlüsselnamen, die mit "G $" beginnen.

Auf private Computer Datenobjekte kann nur über das Betriebssystem zugegriffen werden. Diese Objekte haben Schlüsselnamen, die mit "M $" beginnen.

**Hinweis**  Sie können private Datenobjekte auf dem Computer festlegen, aber nicht abrufen.

Zusätzlich zu diesen Präfixen geben die folgenden Werte auch lokale Objekte oder Computer Objekte an. Diese Werte werden aus Gründen der Abwärtskompatibilität unterstützt und sollten nicht verwendet werden, wenn Sie neue lokale Objekte oder Computer Objekte erstellen. Der Schlüssel Name von lokalen privaten Datenobjekten kann auch mit "rasdialparser" oder "rascreden-" beginnen. Der Schlüssel Name für Computer Objekte kann auch mit "nl $" oder " \_ SC" beginnen \_ .

Bei privaten Datenobjekten, bei denen es sich nicht um einen der vorherigen spezialisierten Typen handelt, werden Schlüsselnamen verwendet, die nicht mit einem Präfix beginnen. Diese Objekte werden nicht repliziert und können entweder lokal oder Remote von Anwendungen gelesen werden.

 

 



