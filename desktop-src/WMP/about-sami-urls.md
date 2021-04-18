---
title: Informationen zu Sami-URLs
description: Informationen zu Sami-URLs
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Windows Media Player, synchronisierter zugänglicher Medienaustausch (Sami)
- Windows Media Player-Objektmodell, synchronisierter zugänglicher Medienaustausch (Sami)
- Objektmodell, synchronisierter, zugänglicher Medienaustausch (Sami)
- Windows Media Player Mobile, synchronisierter verfügbarer Medienaustausch (Sami)
- Windows Media Player ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- Windows Media Player Mobile ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- ActiveX-Steuerelement, synchronisierter, zugänglicher Medienaustausch (Sami)
- Synchronisierter, barrierefreier Medienaustausch (Sami), Dateien
- Samisch (synchronisierter, zugänglicher Medienaustausch), Dateien
- Synchronisierter, barrierefreier Medienaustausch (Sami), URLs
- Samisch (synchronisierter, zugänglicher Medienaustausch), URLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206575"
---
# <a name="about-sami-urls"></a>Informationen zu Sami-URLs

Sami-Dateien können mithilfe einer einzelnen URL digitalen Mediendateien zugeordnet werden. Dies erfolgt mithilfe *des Sami* URL-Parameters. Dem URL-Parameter sind die Basis-URL und eine vorangestellt? befinden. Eine URL mit einem *Sami* -Parameter folgt der folgenden Syntax:

*URL*? *Samisch* = *captionsurl*.

Der Wert des URL-Parameters folgt dem Parameternamen und einem Gleichheitszeichen, wie im folgenden Beispiel gezeigt:


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



Diese URL-Syntax wird häufig in einem Hyperlink oder einer Windows Media-Metadatendatei verwendet, um direkt mit den Speicherorten der digitalen Mediendatei und der Sami-Datei zu verknüpfen. Wenn der Benutzer auf den Link klickt, wird Windows Media Player im vollständigen Modus gestartet und die digitalen Medieninhalte wiedergegeben.

Wenn der *Sami* URL-Parameter nicht angegeben ist, sucht Windows Media Player nach einer Sami-Datei, die sich am gleichen Speicherort wie die digitale Mediendatei befindet und den gleichen Dateinamen hat, mit Ausnahme der Dateinamenerweiterung, die SMI lauten muss. Wenn eine solche Datei vorhanden ist, wird Sie automatisch geöffnet, wenn die Beschriftungs Anzeige im Player aktiviert ist.

Untertitel werden in Windows Media Player aktiviert, indem Sie auf das Menü wieder **Gabe** klicken, dann auf **Beschriftungen und Untertitel** klicken und dann **auf** klicken. Wenn Untertitel aktiviert sind, werden die in der Sami-Datei enthaltenen Beschriftungen angezeigt, während das Medien Element abgespielt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




