---
description: Die Offlineregistrierungsbibliothek wird verwendet, um eine Registrierungsstruktur außerhalb der aktiven Systemregistrierung zu ändern.
ms.assetid: 61db2804-1b67-473f-8dd7-6be6c6a7184e
title: Informationen zur Offlineregistrierungsbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c2aecf71e8e42ad96c018bb613d7aac9a4a867bb301671e9553f1768a4ce44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956179"
---
# <a name="about-the-offline-registry-library"></a>Informationen zur Offlineregistrierungsbibliothek

Die Offlineregistrierungsbibliothek wird verwendet, um eine Registrierungsstruktur außerhalb der aktiven Systemregistrierung zu ändern.

Die Offlineregistrierungsbibliothek ist für Registrierungsupdateszenarien wie die Wartung eines Betriebssystemimages vorgesehen. Die Offlineregistrierungsfunktionen bieten die folgenden Funktionen, die für die Standardregistrierungsfunktionen nicht verfügbar sind:

-   Die Offlineregistrierungsfunktionen können verwendet werden, um eine Registrierungsstruktur in einem beliebigen unterstützten Registrierungsformat zu ändern. Die Standardregistrierungsfunktionen können nur Änderungen an einer aktiven Registrierungsstruktur vornehmen, und die Änderungen müssen mit der Version von Windows kompatibel sein, die auf dem System ausgeführt werden.
-   Die Offlineregistrierungsbibliothek erfordert nur Lesezugriff, um eine Registrierungsstrukturdatei zu öffnen, und Schreibzugriff zum Speichern der Datei. Es werden keine weiteren Zugriffsüberprüfungen für Objekte in der Struktur ausgeführt, sodass die Struktur mit Standardbenutzerberechtigungen geändert werden kann. Mit den Standardregistrierungsfunktionen ist das Laden einer Struktur in die aktive Registrierung ein privilegierter Vorgang, der Administratorzugriff erfordert.

Die Offlineregistrierungsfunktionen sollten aus den folgenden Gründen nicht als Ersatz für die Systemregistrierungsfunktionen verwendet werden:

-   Es ist unmöglich, Registrierungsstrukturen mithilfe der Offlineregistrierungsfunktionen zwischen Prozessen gemeinsam zu nutzen.
-   Die Offlineregistrierungsfunktionen verwenden einfache Sperren, die zu schwerwiegenden Leistungseinbußen für Multithreadanwendungen führen können.
-   Änderungen an den Offlineregistrierungsfunktionen werden erst gespeichert, wenn die [**ORSaveHive-Funktion**](orsavehive.md) aufgerufen wird.

Anwendungen sollten die Offlineregistrierungsfunktionen nicht verwenden, um die Sicherheitsanforderungen der Systemregistrierung zu umgehen. Zum Laden einer Struktur kann eine Anwendung, die ohne die speziellen Berechtigungen ausgeführt wird, die für die [RegLoadKey-Funktion](/windows/win32/api/winreg/nf-winreg-regloadkeya) erforderlich sind, die [RegLoadAppKey-Funktion](/windows/win32/api/winreg/nf-winreg-regloadappkeya) verwenden.

**Windows Server 2003 und Windows XP:** Die [RegLoadAppKey-Funktion](/windows/win32/api/winreg/nf-winreg-regloadappkeya) wird nicht unterstützt.

Eine *Offlineregistrierungsstruktur* ist eine Registrierungsstruktur, die mithilfe der Offlineregistrierungsfunktionen in den Arbeitsspeicher geladen wurde. Verwenden Sie die [**FUNKTION ORCreateHive,**](orcreatehive.md) um eine leere Offlineregistrierungsstruktur zu erstellen. Um eine vorhandene Registrierungsstruktur zu ändern, verwenden Sie die [RegSaveKey-](/windows/win32/api/winreg/nf-winreg-regsavekeya) oder [RegSaveKeyEx-Funktion,](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) um eine Struktur aus der aktiven Systemregistrierung in einer Datei zu speichern, und verwenden Sie dann die [**OROpenHive-Funktion,**](oropenhive.md) um die Datei zu öffnen.

Die Funktionen [**ORCreateHive**](orcreatehive.md) und [**OROpenHive**](oropenhive.md) geben ein Handle für den Stammschlüssel der Offlineregistrierungsstruktur zurück. Dieses Handle kann wie ein Handle für jeden anderen Schlüssel in der Offlineregistrierungsstruktur mit den folgenden Ausnahmen verwendet werden: Die Funktionen [**ORCreateKey**](orcreatekey.md) und [**OROpenKey**](oropenkey.md) können nicht verwendet werden, um ein Handle an den Stammschlüssel zurückzugeben. Die [**ORCloseKey-Funktion**](orclosekey.md) kann nicht zum Schließen des Stammschlüssels verwendet werden. und die [**ORDeleteKey-Funktion**](ordeletekey.md) kann nicht zum Löschen des Stammschlüssels verwendet werden. In all diesen Fällen schlägt die Funktion mit **ERROR \_ INVALID \_ PARAMETER** fehl.

Verwenden Sie die [**ORCreateKey-Funktion,**](orcreatekey.md) um schlüssel zu einer geöffneten Offlineregistrierungsstruktur hinzuzufügen, und die [**ORSetValue-Funktion,**](orsetvalue.md) um die Werte der Schlüssel festzulegen. Die Offlineregistrierungsbibliothek unterstützt andere grundlegende Registrierungsvorgänge wie das Aufzählen, Abrufen und Löschen von Schlüsseln und Werten sowie das Festlegen von Schlüsselattributen wie Sicherheit und Virtualisierungsverhalten. Eine Liste der Funktionen finden Sie unter Funktionen der [Offlineregistrierungsbibliothek.](offline-registry-library-functions.md)

Um Änderungen an einer geöffneten Offlineregistrierungsstruktur zu speichern, verwenden Sie die [**ORSaveHive-Funktion,**](orsavehive.md) um die Struktur in einer Datei zu speichern. (Die Änderungen bleiben nur bestehen, wenn **ORSaveHive** aufgerufen wird.) Verwenden Sie nach dem Speichern der Struktur die [**ORCloseHive-Funktion,**](orclosehive.md) um die Struktur zu schließen und zugeordnete Ressourcen frei zu machen.

Eine Offlineregistrierungsstruktur wird nur überprüft, wenn sie mit der [**OROpenHive-Funktion**](oropenhive.md) geöffnet wird. Wenn die Struktur beschädigt ist, schlägt der Vorgang einfach fehl. es wird nicht versucht, die Struktur zu reparieren. Zugriffsüberprüfungen für Objekte in der Struktur werden erst ausgeführt, wenn die Struktur mit der [RegLoadKey-Funktion](/windows/win32/api/winreg/nf-winreg-regloadkeya) in eine aktive Registrierung geladen wird.

Die Offlineregistrierungsfunktionen unterstützen die [vordefinierten Schlüssel](../sysinfo/predefined-keys.md)nicht.

Alle Schlüssel- und Wertnamenszeichenfolgen, die an Offlineregistrierungsfunktionen übergeben werden, müssen Unicode sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Funktionen der \_ Offlineregistrierungsbibliothek](offline-registry-library-functions.md)
</dt> </dl>

 

 
