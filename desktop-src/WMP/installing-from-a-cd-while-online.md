---
title: Installation von einer CD während der Online Installation
description: Installation von einer CD während der Online Installation
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player Online Stores, Installation von CD, während Online
- Onlinespeicher, Installation von CD, während Online
- Geben Sie 1 Online Stores ein, während Online von CD installiert wird.
- Typ 2 Online Stores, Installation von CD, während Online
- Windows Media Player Online Stores, Online Installationen von CD
- Online-Stores, Online Installationen von CD
- Typ 1 Online Stores, Online Installationen von CD
- Typ 2 Online Stores, Online Installationen von CD
- Windows Media Player Online Stores, CD-Installationen im Online Modus
- Online Stores, CD-Installationen im Online Modus
- Geben Sie 1 Online Stores, CD-Installationen Online ein.
- Geben Sie 2 Online Stores, CD-Installationen Online ein.
- Online-Store von CD in Online Installation installieren
- CD-Installationen von Online Stores im Online Modus
- Online Installationen von Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338393"
---
# <a name="installing-from-a-cd-while-online"></a>Installation von einer CD während der Online Installation

Benutzer können Windows Media Player von einer CD installieren, während Sie mit dem Internet verbunden sind. In diesem Fall findet das Windows Media Player-Setup das vom *serviceInfo* -Befehlszeilenparameter angegebene serviceInfo-Dokument. Wenn das **Schlüssel** Attribut mit dem *defaultservice* -Befehlszeilenparameter übereinstimmt, prüft Setup das install-Element, um den Setup Vorgang anzupassen. Wenn Sie die Attributwerte verwenden, werden Ihre Endbenutzer-Lizenzbedingungen (EULA) und ihre Datenschutzbestimmungen angezeigt. Außerdem wird die CAB-Datei auf dem Computer des Benutzers abgerufen und installiert. Beispielsweise können Sie diese Funktion verwenden, um die neueste Version eines COM-Objekts zu installieren, das für den Online Shop erforderlich ist.

Nachdem es installiert wurde, legt Windows Media Player den anfänglichen Online Store mithilfe des Schlüssel namensfest, den Sie für den *defaultservice* -Befehlszeilenparameter angegeben haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Install-Element**](install-element.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> <dt>

[**Festlegen des ersten Online Stores**](setting-the-initial-online-store.md)
</dt> <dt>

[**Einrichten von Befehlszeilen Parametern für Online Stores**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




