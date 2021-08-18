---
title: Installieren von einer CD während der Online-Installation
description: Installieren von einer CD während der Online-Installation
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player,Installation von CD während der Online-Installation
- Onlineshops,Installation von CD während der Online-Installation
- Geben Sie 1 Onlineshops ein, die von CD installiert werden, während sie online sind.
- Geben Sie 2 Onlineshops ein, und installieren Sie sie über cd, während sie online sind.
- Windows Media Player online stores,online installs from CD (Online-Installationen von CD)
- Onlineshops,Online-Installationen von CD
- Typ 1 Onlineshops,Online-Installationen von CD
- 'Typ 2: Onlineshops,Online-Installationen von CD'
- Windows Media Player Onlinespeicher,CD wird installiert
- Onlineshops,CD-Installationen, während sie online sind
- Geben Sie 1 Onlineshops ein, CD wird während der Online-Installation installiert.
- 'Typ 2: Onlineshops, CD-Installationen während der Online'
- Installieren von Onlineshops über CD während der Online-Installation
- CD-Installationen von Onlineshops im Onlinespeicher
- Online-Installationen von Onlineshops
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13589d7ba6dea0693acaacb5e0d1f551b4a4f178c4ccb50a1bd8ebb513dda3de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996510"
---
# <a name="installing-from-a-cd-while-online"></a>Installieren von einer CD während der Online-Installation

Benutzer können die Windows Media Player über eine CD installieren, während sie mit dem Internet verbunden sind. In diesem Fall sucht Windows Media Player Setup das ServiceInfo-Dokument, das durch den *ServiceInfo-Befehlszeilenparameter* angegeben wird. Wenn das **Key-Attribut** dem *DefaultService-Befehlszeilenparameter* entspricht, überprüft setup das Install-Element, um den Setupprozess anzupassen. Mithilfe der Attributwerte zeigt Setup Ihren Endbenutzer-Lizenzvertrag (EULA) und Ihre Datenschutzerklärung an und ruft ihre .cab-Datei auf dem Computer des Benutzers ab und installiert sie. Sie können dieses Feature beispielsweise verwenden, um die neueste Version eines COM-Objekts zu installieren, das für Ihren Onlineshop erforderlich ist.

Nach der Installation legt Windows Media Player den ursprünglichen Onlineshop mithilfe des Schlüsselnamens fest, den Sie für den *DefaultService-Befehlszeilenparameter* angegeben haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Install-Element**](install-element.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> <dt>

[**Festlegen des anfänglichen Online-Store**](setting-the-initial-online-store.md)
</dt> <dt>

[**Einrichten von Befehlszeilenparametern für Onlineshops**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




