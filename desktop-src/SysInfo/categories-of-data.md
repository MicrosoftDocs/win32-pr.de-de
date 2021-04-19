---
description: 'Vor dem Einfügen von Daten in die Registrierung sollte eine Anwendung die Daten in zwei Kategorien unterteilen: Computer spezifische Daten und benutzerspezifische Daten.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Datenkategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357117"
---
# <a name="categories-of-data"></a>Datenkategorien

Vor dem Einfügen von Daten in die Registrierung sollte eine Anwendung die Daten in zwei Kategorien unterteilen: Computer spezifische Daten und benutzerspezifische Daten. Durch diese Unterscheidung kann eine Anwendung mehrere Benutzer unterstützen und dennoch benutzerspezifische Daten über ein Netzwerk suchen und diese Daten an verschiedenen Speicherorten verwenden, sodass standortunabhängige Benutzerprofil Daten möglich sind. (Ein Benutzerprofil ist ein Satz von Konfigurationsdaten, die für jeden Benutzer gespeichert werden.)

Wenn die Anwendung installiert ist, sollten Sie die computerspezifischen Daten unter dem Schlüssel **HKEY \_ local \_ Machine** aufzeichnen. Insbesondere sollten Schlüssel für den Firmennamen, den Produktnamen und die Versionsnummer erstellt werden, wie im folgenden Beispiel gezeigt:

**HKEY \_ \_ \\ Software \\ für den lokalen Computer**_MyCompany \\ MyProduct \\ 1,0_

Wenn die Anwendung com unterstützt, sollte diese Daten unter **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** aufgezeichnet werden.

Eine Anwendung sollte benutzerspezifische Daten mit dem **aktuellen HKEY- \_ \_ Benutzer** Schlüssel aufzeichnen, wie im folgenden Beispiel gezeigt:

**HKEY \_ Aktuelle \_ Benutzer \\ Software \\**_MyCompany \\ MyProduct \\ 1,0_

 

 



