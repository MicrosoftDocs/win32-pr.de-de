---
description: Geschützter Speicher bietet Anwendungen eine Schnittstelle zum Speichern von Benutzerdaten, die sicher oder von Änderungen getrennt aufbewahrt werden müssen.
ms.assetid: 85c1a009-c4f7-4b5a-ad96-6845a4e80de9
title: PStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d291b911c351cce10827b7937c6a474b7c570
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340099"
---
# <a name="pstore"></a>PStore

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Geschützter Speicher bietet Anwendungen eine Schnittstelle zum Speichern von Benutzerdaten, die sicher oder von Änderungen getrennt aufbewahrt werden müssen.

Dateneinheiten werden als Elemente bezeichnet. Die Struktur und der Inhalt der gespeicherten Daten sind für das geschützte Speichersystem nicht transparent. Der Zugriff auf Elemente unterliegt der Bestätigung gemäß einem benutzerdefinierten Sicherheits Stil, der angibt, welche Bestätigung für den Zugriff auf die Daten erforderlich ist, z. b. ob ein Kennwort erforderlich ist. Außerdem unterliegt der Zugriff auf Elemente einem Zugriffs Regelsatz. Es gibt eine Zugriffs Regel für jeden Zugriffsmodus: z. b. "Lesen/Schreiben". Zugriffs Regelsätze bestehen aus Zugriffs Klauseln. Derzeit werden zwei Arten von Zugriffs Klauseln unterstützt: Authenticode und binäre Überprüfung des Aufrufers. In der Regel wird zum Zeitpunkt der Anwendungs Einrichtung ein Mechanismus bereitgestellt, mit dem eine neue Anwendung den Benutzer Zugriff auf Elemente anfordern kann, die zuvor von einer anderen Anwendung erstellt wurden.

Elemente werden durch die Kombination aus Schlüssel, Typ, Untertyp und Name eindeutig identifiziert. Der Schlüssel ist eine Konstante, die angibt, ob das Element für diesen Computer Global ist oder nur diesem Benutzer zugeordnet ist. Der Name ist eine Zeichenfolge, die in der Regel vom Benutzer ausgewählt wird. Typ und Untertyp sind **GUID** s, die in der Regel von der Anwendung angegeben werden. Weitere Informationen zu Typen und Untertypen werden in der Systemregistrierung beibehalten und enthalten Attribute wie Anzeige Name und UI-Hinweise. Bei Untertypen ist der übergeordnete Typ korrigiert und in der Systemregistrierung als Attribut enthalten. Die typgruppenelemente werden für einen allgemeinen Zweck verwendet: z. b. Zahlung oder Identifikation. Die untergeordneten Gruppenelemente haben ein gemeinsames Datenformat.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**Iumumpstoreitems**](ienumpstoreitems.md)
-   [**Ienumpstoreproviders**](ienumpstoreproviders.md)
-   [**Iumumpstoretypes**](ienumpstoretypes.md)
-   [**Ipstore**](ipstore.md)
-   [**Pstorecreatanstance**](pstorecreateinstance.md)
-   [**Pstoreenumproviders**](pstoreenumproviders.md)
-   [**Pstore-Konstanten**](pstore-constants.md)
-   [**Pstore-Typen**](pstore-types.md)

 

 
