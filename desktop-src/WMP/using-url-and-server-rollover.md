---
title: Verwenden von URL-und Serverrollover
description: Verwenden von URL-und Serverrollover
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Windows Media Metadatei-Wiedergabelisten, URL-Rollover
- Wiedergabelisten, URL-Rollover
- Metadatei-Wiedergabelisten, URL-Rollover
- Windows Media Metadatei-Wiedergabelisten, Serverrollover
- Wiedergabelisten, Serverrollover
- Metadatei-Wiedergabelisten, Serverrollover
- Windows Media Metadatei-Wiedergabelisten, Protokollrollover
- Wiedergabelisten, Protokollrollover
- Metadatei-Wiedergabelisten, Protokollrollover
- Windows Media Player, URL-Rollover
- Windows Media Player, Serverrollover
- Windows Media Player, Protokollrollover
- URL-Rollover
- Serverrollover
- Protokollrollover
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310168"
---
# <a name="using-url-and-server-rollover"></a>Verwenden von URL-und Serverrollover

Mithilfe von Metadatei-Wiedergabelisten können Sie ein automatisches Rollback zu alternativen Inhalts Quellen bereitstellen, wenn auf einen Stream nicht zugegriffen oder wiedergegeben werden kann. Mit dieser Rollover-Methode können Sie Quellen desselben Inhalts auf unterschiedlichen Servern oder unterschiedlichen Server Typen angeben. Sie können z. b. eine erste Alternative auf einem anderen Windows Media-Server angeben. Wenn diese Inhalte nicht wiedergegeben werden können, kann der Client ein Rollback auf eine zweite Alternative auf einem Webserver ausführen. Windows Media Player versucht automatisch, gemäß seinen Windows Media-Eigenschafts Einstellungen ein Rollback auf verschiedene Protokolle auszuführen, bevor die Rollover-URLs in der Wiedergabeliste ausprobiert werden.

Legen Sie Server-und Protokollrollover fest, indem Sie mehrere **ref** -Elemente nacheinander innerhalb eines **Eintrags** Elements platzieren. Jedes **ref** -Element gibt einen alternativen Speicherort oder ein alternatives Protokoll für eine Mediendatei oder einen Datenstrom an.

Beispielcode


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metafile-Wiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> </dl>

 

 




