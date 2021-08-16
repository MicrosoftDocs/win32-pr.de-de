---
title: Installieren aus dem Web während der Online-Installation
description: Installieren aus dem Web während der Online-Installation
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player Onlinespeicher,Installation über das Web
- Onlineshops,Installation über das Web während der Online-Installation
- Geben Sie 1 Onlineshops ein, und installieren Sie sie über das Web, während sie online sind.
- Typ 2 Onlineshops,Installation über das Web während der Online-Installation
- Windows Media Player,Online-Installationen aus dem Web
- Onlineshops,Online-Installationen aus dem Web
- 'Typ 1: Onlineshops,Online-Installationen aus dem Web'
- 'Typ 2: Onlineshops,Online-Installationen aus dem Web'
- Installieren von Onlineshops aus dem Web während der Online-Installation
- Online-Installationen von Onlineshops
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801dd9fbee8bff2660a39f6b40e8a5a9e703df00f82be54a7b93c0d200d2ccea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135553"
---
# <a name="installing-from-the-web-while-online"></a>Installieren aus dem Web während der Online-Installation

Benutzer können Windows Media Player Webdownload installieren, während sie mit dem Internet verbunden sind. In diesem Fall kann Microsoft den ursprünglichen Onlineshop konfigurieren, den Sie angeben.

Verwenden Sie die Windows Media Player URL, um die Daten auf diese Weise neu zu verteilen:

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*Version*&UserLocale=*localID*&Service=-Schlüssel

Legen Sie in der  vorherigen URL den Schlüssel auf den Schlüsselnamen für Ihren Onlineshop und *localeID* auf den Bezeichner des Orts fest, in dem Ihr Speicher den Dienst bietet. Legen *Sie version* auf 2 für Windows Media Player 11 auf Windows XP oder 1 für Windows Media Player 10 fest. Die URL installiert Windows Media Player und legt den anfänglichen aktiven Speicher auf den durch den Schlüssel angegebenen *fest.*

Das folgende Beispiel zeigt eine URL, die Windows Media Player 11 installiert und Proseware als ersten aktiven Speicher fest legt. Der Wert 409 für *localeID* gibt an, dass Proseware den Dienst in der USA.

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

Wenn das ServiceInfo-Dokument für den Onlineshop ein Install-Element enthält, wird Windows Media Player Setup den Setupprozess anpassen. Mithilfe der Attributwerte zeigt Setup Ihren Endbenutzer-Lizenzvertrag (EULA) und Ihre Datenschutzerklärung an und ruft ihre .cab-Datei auf dem Computer des Benutzers ab und installiert sie. Sie können dieses Feature beispielsweise verwenden, um die neueste Version eines COM-Objekts zu installieren, das für Ihren Onlineshop erforderlich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Install-Element**](install-element.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> <dt>

[**Festlegen des anfänglichen Online-Store**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




