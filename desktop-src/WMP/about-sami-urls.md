---
title: Informationen zu SAMI-URLs
description: Informationen zu SAMI-URLs
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Windows Media Player,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Objektmodell, Synchronized Accessible Media Interchange (SAMI)
- Objektmodell,Synchronisierter austauschbarer Medienaustausch (SAMI)
- Windows Media Player Mobiler, synchronisierter austauschbarer Medienaustausch (SAMI)
- Windows Media Player ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Mobile ActiveX,Synchronized Accessible Media Interchange (SAMI)
- ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Synchronized Accessible Media Interchange (SAMI),files
- SAMI (Synchronized Accessible Media Interchange), Files
- Synchronisierter austauschbarer Medienaustausch (SAMI), URLs
- SAMI (Synchronized Accessible Media Interchange), URLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a35976c6988ad4298c812005002da010730d5254bd7c010f24fe32741be393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956800"
---
# <a name="about-sami-urls"></a>Informationen zu SAMI-URLs

SAMI-Dateien können digitalen Mediendateien über eine einzelne URL zugeordnet werden. Dies wird mithilfe des *Sami-URL-Parameters* erreicht. Dem URL-Parameter sind die Basis-URL und ein vorangehendes ? befinden. Eine URL mit einem *sami-Parameter* folgt dieser Syntax:

*URL*? *sami* = *captionsURL*.

Der Wert des URL-Parameters folgt dem Parameternamen und einem Gleichheitszeichen, wie im folgenden Beispiel:


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



Diese URL-Syntax wird häufig in einem Link oder einer Windows Media-Metadatei verwendet, um direkt mit den Speicherorten der digitalen Mediendatei und der SAMI-Datei zu verknüpfen. Wenn der Benutzer auf den Link klickt, Windows Media Player im voll verfügbaren Modus gestartet und gibt den Inhalt der digitalen Medien wieder.

Wenn der *Parameter sami* URL nicht angegeben ist, sucht Windows Media Player nach einer SAMI-Datei, die sich am gleichen Speicherort wie die digitale Mediendatei befindet und denselben Dateinamen hat, mit Ausnahme der Dateierweiterung, die SMI sein muss. Wenn eine solche Datei vorhanden ist, wird sie automatisch geöffnet, wenn die Beschriftungsanzeige im Player aktiviert wurde.

Untertitel werden in Windows Media Player aktiviert, indem Sie  auf das Menü Wiederklicken, dann auf Untertitel und Untertitel und dann auf **Ein klicken.** Wenn Untertitel aktiviert sind, werden die in der SAMI-Datei enthaltenen Untertitel angezeigt, während das Medienelement abspielt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




