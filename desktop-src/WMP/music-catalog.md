---
title: Musikkatalog
description: Musikkatalog
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player Online Stores, Musikkataloge
- Online Stores, Musikkataloge
- Typ 1 Online Stores, Musikkataloge
- Windows Media Player Online Stores, Katalog Compiler
- Online Stores, Katalog Compiler
- Typ 1 Online Stores, Katalog Compiler
- Musikkataloge
- Katalog Compiler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038526"
---
# <a name="music-catalog"></a>Musikkatalog

Ein Onlinespeicher vom Typ 1 erstellt seinen Musikkatalog als Satz von TSV-Dateien (Registerkarten getrennte Werte). Der Online Shop verwendet den [Katalog Compiler](catalog-compiler-for-type-1-online-stores.md) von Microsoft, um die TSV-Dateien in einen komprimierten Katalog zu kompilieren, der von Windows Media Player heruntergeladen werden kann. Windows Media Player können vollständige Katalogdateien oder Katalog Update Dateien herunterladen. Katalog Updates enthalten nur die Katalog Informationen, die seit dem letzten Katalog Update geändert wurden. Das Inhalts Partner-Plug-in kann feststellen, ob ein vollständiger Katalog oder ein Update heruntergeladen werden soll. In beiden Fällen wendet Windows Media Player die Änderungen auf den aktuellen Katalog an, wenn eine Benachrichtigung vom Plug-in vorliegt.

Wenn für den Online Store ein neuer Katalog vorbereitet wurde, kann das Plug-in den Spieler Benachrichtigen, indem er [iwmpcontentpartnercallback:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) aufrufen und wmpcnnewcatalogavailable als Wert für den *Typparameter* übergibt.

Wenn Windows Media Player zum Herunterladen eines Katalogs oder Updates bereit ist, ruft der Player [iwmpcontentpartner:: getcatalogurl](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)auf. Diese Methode stellt dem Plug-in Informationen zum aktuellen Katalog zur Verfügung, z. b. die Katalogversion und die Gebiets Schema-ID. Das Plug-in antwortet durch Bereitstellen der URL (Uniform Resource Serverlocatorpunkt) des korrekten vollständigen Katalogs oder Updates sowie einer aktualisierten Versionsnummer und Ablaufdatum. Windows Media Player fordert regelmäßig Katalog Updates basierend auf den Informationen an, die vom Plug-in in **getcatalogurl** bereitgestellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 1 Online Stores**](about-type-1-online-stores.md)
</dt> <dt>

[**Katalog Compiler für Typ 1-Online Speicher**](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[**Iwmpcontentpartner-Schnittstelle**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




