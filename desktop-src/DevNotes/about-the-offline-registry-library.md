---
description: Die Offline Registrierungs Bibliothek wird zum Ändern einer Registrierungs Struktur außerhalb der aktiven Systemregistrierung verwendet.
ms.assetid: 61db2804-1b67-473f-8dd7-6be6c6a7184e
title: Informationen zur Offline Registrierungs Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e08b401a4a77f55a54c48ad147bf38c8796472
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482854"
---
# <a name="about-the-offline-registry-library"></a>Informationen zur Offline Registrierungs Bibliothek

Die Offline Registrierungs Bibliothek wird zum Ändern einer Registrierungs Struktur außerhalb der aktiven Systemregistrierung verwendet.

Die Offline Registrierungs Bibliothek ist für Registrierungs Aktualisierungs Szenarien wie die Wartung eines Betriebssystem Abbilds vorgesehen. Die Funktionen der Offline Registrierung bieten die folgenden Funktionen, die mit den standardmäßigen Registrierungsfunktionen nicht verfügbar sind:

-   Die Offline Registrierungsfunktionen können verwendet werden, um eine Registrierungs Struktur in einem beliebigen unterstützten Registrierungs Format zu ändern. Die Standard Registrierungsfunktionen können nur Änderungen an einer aktiven Registrierungs Struktur vornehmen, und die Änderungen müssen mit der Windows-Version kompatibel sein, die auf dem System ausgeführt wird.
-   Die Offline Registrierungs Bibliothek erfordert nur Lesezugriff, um eine Registrierungs Struktur Datei zu öffnen und Schreibzugriff zum Speichern der Datei zu erhalten. Für Objekte in der Hive werden keine weiteren Zugriffs Überprüfungen durchgeführt, sodass die Hive mit Standardbenutzer Berechtigungen geändert werden kann. Mit den Standard Registrierungsfunktionen ist das Laden einer Hive in die aktive Registrierung ein privilegierter Vorgang, der administrativen Zugriff erfordert.

Die Offline Registrierungsfunktionen sollten aus folgenden Gründen nicht als Ersatz für die System Registrierungsfunktionen verwendet werden:

-   Es ist nicht möglich, Registrierungs Strukturen mithilfe der Offline Registrierungsfunktionen zwischen Prozessen freizugeben.
-   Die Offline Registrierungsfunktionen verwenden einfache sperren, die zu einer schwerwiegenden Beeinträchtigung der Leistung bei Multithreadanwendungen führen können.
-   Änderungen, die mit den Offline Registrierungsfunktionen vorgenommen werden, werden erst gespeichert, wenn die [**orsavehive**](orsavehive.md) -Funktion aufgerufen wird.

Anwendungen sollten die Offline Registrierungsfunktionen nicht verwenden, um die Sicherheitsanforderungen der Systemregistrierung zu umgehen. Zum Laden einer Hive kann eine Anwendung, die ohne spezielle Berechtigungen ausgeführt wird, die von der [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) -Funktion benötigt wird, die [regloadappkey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) -Funktion verwenden.

**Windows Server 2003 und Windows XP:** Die [regloadappkey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) -Funktion wird nicht unterstützt.

Eine *Offline Registrierungs* Struktur ist eine Registrierungs Struktur, die mithilfe der Offline Registrierungsfunktionen in den Arbeitsspeicher geladen wurde. Um eine leere Offline Registrierungs Struktur zu erstellen, verwenden Sie die [**orkreatehive**](orcreatehive.md) -Funktion. Verwenden Sie zum Ändern einer vorhandenen Registrierungs Struktur die [regsavekey](/windows/win32/api/winreg/nf-winreg-regsavekeya) -oder [regsavekeyex](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) -Funktion, um eine Hive aus der aktiven Systemregistrierung in einer Datei zu speichern, und verwenden Sie dann die [**oropenhive**](oropenhive.md) -Funktion, um die Datei zu öffnen.

Die [**orkreatehive**](orcreatehive.md) -und [**oropenhive**](oropenhive.md) -Funktionen geben ein Handle für den Stamm Schlüssel der Offline Registrierungs Struktur zurück. Dieses Handle kann wie ein Handle für einen beliebigen anderen Schlüssel in der Offline Registrierungs Struktur mit den folgenden Ausnahmen verwendet werden: die [**orkreatekey**](orcreatekey.md) -und [**oropenkey**](oropenkey.md) -Funktionen können nicht verwendet werden, um ein Handle für den Stamm Schlüssel zurückzugeben. die [**orclosekey**](orclosekey.md) -Funktion kann nicht verwendet werden, um den Stamm Schlüssel zu schließen. und die [**ordeletekey**](ordeletekey.md) -Funktion kann nicht zum Löschen des Stamm Schlüssels verwendet werden. In allen diesen Fällen schlägt die Funktion fehl, und es wird ein **\_ ungültiger \_ Parameter angezeigt**.

Verwenden Sie die [**orkreatekey**](orcreatekey.md) -Funktion, um Schlüssel zu einer geöffneten Offline Registrierungs Struktur hinzuzufügen, und die [**orsetvalue**](orsetvalue.md) -Funktion, um die Schlüsselwerte festzulegen. Die Offline Registrierungs Bibliothek unterstützt weitere grundlegende Registrierungs Vorgänge, wie z. b. das auflisten, abrufen und Löschen von Schlüsseln und Werten und das Festlegen von Schlüssel Attributen, wie z. b. Sicherheits-und Virtualisierungsverhalten. Eine Liste der Funktionen finden Sie unter [Funktionen der Offline-Registrierungs Bibliothek](offline-registry-library-functions.md).

Um an einer geöffneten Offline Registrierungs Struktur vorgenommene Änderungen zu speichern, verwenden Sie die [**orsavehive**](orsavehive.md) -Funktion, um die Struktur in einer Datei zu speichern. (Die Änderungen bleiben nicht bestehen, es sei denn, **orsavehive** wird aufgerufen.) Verwenden Sie nach dem Speichern der Hive die [**orclosehive**](orclosehive.md) -Funktion, um die Hive und die damit verbundenen Ressourcen zu schließen.

Eine Offline Registrierungs Struktur wird nur überprüft, wenn Sie mit der [**oropenhive**](oropenhive.md) -Funktion geöffnet wird. Wenn die Hive beschädigt ist, schlägt der Vorgang einfach fehl. Es wird nicht versucht, die Hive zu reparieren. Zugriffs Überprüfungen für Objekte in der Struktur werden erst ausgeführt, wenn die Hive mit der [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) -Funktion in eine aktive Registrierung geladen wurde.

Die [vordefinierten Schlüssel](../sysinfo/predefined-keys.md)werden von den Funktionen der Offline Registrierung nicht unterstützt.

Alle Schlüssel-und Wert Namen Zeichenfolgen, die an Offline Registrierungsfunktionen übermittelt werden, müssen Unicode sein

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Funktionen der Offline-Registrierungs Bibliothek \_](offline-registry-library-functions.md)
</dt> </dl>

 

 
