---
title: Musik Katalog
description: Musik Katalog
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player Onlineshops, Musikkataloge
- Onlineshops, Musikkataloge
- Geben Sie 1 Onlineshops ein, Musikkataloge
- Windows Media Player Onlineshops, Katalogcompiler
- Onlineshops, Katalogcompiler
- Typ 1 Onlineshops, Katalogcompiler
- Musikkataloge
- Katalogcompiler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2474204686a498c81ec12b87daeba99f21397492dc5178a70580d4a37750d9cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123300"
---
# <a name="music-catalog"></a>Musik Katalog

Ein Onlineshop vom Typ 1 erstellt seinen Musikkatalog als Gruppe von TSV-Dateien (Tab-Separated Value). Anschließend verwendet der Onlineshop den [Katalogcompiler](catalog-compiler-for-type-1-online-stores.md) von Microsoft, um die TSV-Dateien in einen komprimierten Katalog zu kompilieren, der von Windows Media Player heruntergeladen werden kann. Windows Media Player können vollständige Katalogdateien oder Katalogupdatedateien herunterladen. Katalogupdates enthalten nur die Kataloginformationen, die sich seit dem letzten Katalogupdate geändert haben. Es obliegt dem Inhaltspartner-Plug-In, zu bestimmen, ob ein vollständiger Katalog oder ein Update heruntergeladen werden soll. In beiden Fällen wendet Windows Media Player die Änderungen nach Benachrichtigung vom Plug-In auf den aktuellen Katalog an.

Wenn im Onlineshop ein neuer Katalog vorbereitet wurde, kann das Plug-In den Player benachrichtigen, indem [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) aufgerufen und wmpcnNewCatalogAvailable als Wert für den *Typparameter* übergeben wird.

Wenn Windows Media Player bereit ist, einen Katalog oder ein Update herunterzuladen, ruft der Player [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)auf. Diese Methode stellt dem Plug-In Informationen zum aktuellen Katalog bereit, z. B. die Katalogversion und den Gebietsschemabezeichner. Das Plug-In reagiert, indem der einheitliche Ressourcenlocator (URL) des richtigen vollständigen Katalogs oder Updates sowie eine aktualisierte Versionsnummer und ein Ablaufdatum angegeben werden. Windows Media Player fordert in regelmäßigen Abständen Katalogupdates basierend auf den Informationen an, die vom Plug-In **GetCatalogURL** bereitgestellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Onlineshops vom Typ 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Katalogcompiler für Onlineshops vom Typ 1**](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentPartner-Schnittstelle**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




