---
description: Wenn ein Dokument oder Text durch einen einzelnen Benutzer geschützt werden muss oder wenn das Dokument von einer kleinen Gruppe von Benutzern gemeinsam genutzt werden muss, die alle Zugriff auf das gleiche geheime Kennwort haben, kann eine einfache Verschlüsselung/Entschlüsselung durchgeführt werden.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Verschlüsseln und Entschlüsseln von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960378"
---
# <a name="encrypting-and-decrypting-data"></a>Verschlüsseln und Entschlüsseln von Daten

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Wenn ein Dokument oder Text durch einen einzelnen Benutzer geschützt werden muss oder wenn das Dokument von einer kleinen Gruppe von Benutzern gemeinsam genutzt werden muss, die alle Zugriff auf das gleiche geheime Kennwort haben, kann eine einfache Verschlüsselung/Entschlüsselung durchgeführt werden. CAPICOM unterstützt den PKCS \# 7-Inhaltstyp "verschlüsselteddata" nicht, sondern verwendet eine nicht standardmäßige ASN-Struktur für "verschlüsselteddata". Daher kann nur CAPICOM ein CAPICOM-Objekt "verschlüsselteddata" entschlüsseln.

In den folgenden Abschnitten werden Beispiele für Verschlüsselungs-und Entschlüsselungs Aufgaben veranschaulicht:

-   [Verschlüsseln einer Nachricht in CAPICOM](encrypting-a-message-in-capicom.md)
-   [Entschlüsseln einer Nachricht in CAPICOM](decrypting-a-message-in-capicom.md)

 

 



