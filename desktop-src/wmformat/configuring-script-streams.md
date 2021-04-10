---
title: Konfigurieren von Skript Datenströmen
description: Konfigurieren von Skript Datenströmen
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- Streams, Konfigurieren von Skript Datenströmen
- Codecs, Konfigurieren von Skript Datenströmen
- Skripterstellung, konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036835"
---
# <a name="configuring-script-streams"></a>Konfigurieren von Skript Datenströmen

Wie bei allen beliebigen Streamtypen müssen für Skript Datenströme eine Bitrate und ein Puffer Fenster definiert werden. Der Haupt Medientyp in der [**WM \_ - \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur muss auf wmmediatype-Skript festgelegt werden \_ .

Für Skript Datenströme muss der **Format Type** -Member des **WM- \_ Medien \_ Typs** auf wmformat-Skript festgelegt sein \_ , was darauf hinweist, dass der **pbformat** -Member auf eine [**wmscriptformat**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) -Struktur verweist.

Es gibt nur einen unterstützten Skripttyp, wmscripttype \_ twostrings.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Konfiguration für alle Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Skriptbefehle**](script-commands.md)
</dt> </dl>

 

 




