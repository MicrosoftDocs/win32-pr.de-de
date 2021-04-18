---
title: Installation über das Web während der Online Installation
description: Installation über das Web während der Online Installation
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player Online Stores, die Installation über das Web während der Online Dokumentation
- Online Stores, Installation über das Web während der Online Dokumentation
- Geben Sie 1 Online Stores ein, und installieren Sie Sie online.
- Geben Sie 2 Online Stores ein, und installieren Sie Sie online.
- Windows Media Player Online Stores, Online Installationen aus dem Web
- Online-Stores, Online Installationen aus dem Web
- Typ 1 Online Stores, Online Installationen aus dem Web
- Typ 2 Online Stores, Online Installationen aus dem Web
- Online-Stores werden online aus dem Web installiert.
- Online Installationen von Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341459"
---
# <a name="installing-from-the-web-while-online"></a>Installation über das Web während der Online Installation

Benutzer können Windows Media Player als Webdownload installieren, während eine Verbindung mit dem Internet besteht. In diesem Fall kann Microsoft den von Ihnen angegebenen anfänglichen Onlinespeicher konfigurieren.

Verwenden Sie zum erneuten Verteilen von Windows Media Player auf diese Weise die folgende URL:

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*Version*&UserLocale =*localId*&Service =*Key*

Legen Sie in der vorangehenden URL *Key* auf den Schlüsselnamen für Ihren Online Store fest, und legen Sie *LocaleID* auf den Bezeichner des Gebiets Schemas fest, in dem der Speicherdienst bereitstellt. Legen Sie für Windows Media Player 11 unter Windows XP oder 1 für Windows Media Player 10 *Version* auf 2 fest. Die URL installiert Windows Media Player und legt den ersten aktiven Speicher auf den durch *Key* angegebenen Wert fest.

Das folgende Beispiel zeigt eine URL, mit der Windows Media Player 11 installiert wird und Proseware als ersten aktiven Speicher festgelegt wird. Der Wert 409 für *LocaleID* gibt an, dass Proseware Dienst im USA bereitstellt.

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

Wenn das serviceInfo-Dokument für den Online Shop ein install-Element enthält, wird der Setup Vorgang von Windows Media Player Setup angepasst. Wenn Sie die Attributwerte verwenden, werden Ihre Endbenutzer-Lizenzbedingungen (EULA) und ihre Datenschutzbestimmungen angezeigt. Außerdem wird die CAB-Datei auf dem Computer des Benutzers abgerufen und installiert. Beispielsweise können Sie diese Funktion verwenden, um die neueste Version eines COM-Objekts zu installieren, das für den Online Shop erforderlich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Install-Element**](install-element.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> <dt>

[**Festlegen des ersten Online Stores**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




