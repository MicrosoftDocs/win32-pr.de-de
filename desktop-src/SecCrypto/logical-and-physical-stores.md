---
description: Standardsystem Speicher, einschließlich "My", "ca" und "root", werden als logische Sammlungs Speicher mit einer Reihe von vordefinierten physischen Speichern als Mitglieder Speicher implementiert.
ms.assetid: 1d82b94b-4842-454a-aca4-823cd264ac52
title: Logische und physische Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a5441bac91e39b7f4c124daecd3a6a569c323c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752137"
---
# <a name="logical-and-physical-stores"></a>Logische und physische Speicher

Standardsystem Speicher, einschließlich "My", "ca" und "root", werden als logische Sammlungs Speicher mit einer Reihe von vordefinierten physischen Speichern als Mitglieder Speicher implementiert. Die physischen Speicher Mitglieder eines System Speichers werden automatisch geöffnet, wenn der Systemspeicher geöffnet wird. Ein Benutzer kann einer beliebigen Systemspeicher Sammlung weitere physische Speicher hinzufügen. Die CryptoAPI-Funktion [**certregisterphysicalstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore) fügt einer Systemspeicher Auflistung einen neuen physischen Speicher hinzu. [**Certunregisterphysicalstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore) trennt einen physischen Speicher von einem logischen Systemspeicher. [**Certregistersystemstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore) erstellt einen neuen Systemspeicher unter einem Registrierungs-HKEY, während [**certunregistersystemstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore) einen Systemspeicher aus der Registrierung entfernt.

In CryptoAPI sind Systemspeicher logische Speicher mit zugeordneten physischen speichern. Alle Zertifikate in einem vorhandenen Systemspeicher sind weiterhin verfügbar, und das physische Hinzufügen neuer Zertifikate wird in den physischen Speichern vorgenommen, aus denen der logische Systemspeicher besteht.

Benutzer, die weiterhin physische Systemspeicher verwenden und nicht in logische Speicher konvertieren möchten, können Systemspeicher mit dem Zertifikat \_ Speicher \_ Prov- \_ System \_ Registrierungs Anbieter öffnen. Dieser Anbieter verwendet weiterhin jeden Systemspeicher als einen einzelnen physischen Speicher.

Die Funktionen [**certenumschlag systemstoreloations**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation), [**certenumschlag**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)und [**certenumschlag physicalstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) Listensystem Speicherorte, verfügbare Systemspeicher und alle physischen Speicher auf, die Mitglieder eines System Speichers sind.

System Speicher können auch verschoben werden. Standardmäßig wird ein Systemspeicher in Relation zu einem Registrierungs Unterschlüssel geöffnet, der einem vordefinierten Muster folgt. Weitere Informationen finden Sie unter [System Speicherorte](system-store-locations.md). \_ \_ Durch das Festlegen des \_ Zertifikats zum Verschieben von Zertifikat System Speicher \_ im *dwFlags* -Parameter, der an [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) übergeben wird, wird ein System Speicher in der Registrierung unter einem vom Benutzer angegebenen Registrierungs Unterschlüssel anstelle des vordefinierten Registrierungs unter Schlüssels platziert.

 

 



