---
title: Verwenden von URL und Serverrollover
description: Verwenden von URL und Serverrollover
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Windows Medienmetadatei-Wiedergabelisten, URL-Rollover
- Wiedergabelisten, URL-Rollover
- Metafile-Wiedergabelisten, URL-Rollover
- Windows Medienmetadatei-Wiedergabelisten, Serverrollover
- Wiedergabelisten, Serverrollover
- Metafile-Wiedergabelisten, Serverrollover
- Windows Medienmetadatei-Wiedergabelisten, Protokollrollover
- Wiedergabelisten, Protokollrollover
- Metafile-Wiedergabelisten, Protokollrollover
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
ms.openlocfilehash: 3988ff019fba838e86ea1d0e7b0f6124c367bb8b505a0f2d2e2f639b94d93e52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465674"
---
# <a name="using-url-and-server-rollover"></a>Verwenden von URL und Serverrollover

Sie können Metadateiwiedergabelisten verwenden, um ein automatisches Rollback auf alternative Inhaltsquellen bereitzustellen, wenn auf einen Stream nicht zugegriffen oder wiedergegeben werden kann. Sie können diese Rollovermethode verwenden, um Quellen desselben Inhalts auf verschiedenen Servern oder verschiedenen Servertypen anzugeben. Sie können z. B. eine erste Alternative auf einem anderen Windows Medienserver angeben. Wenn dieser Inhalt nicht wiedergegeben werden kann, kann der Client ein Rollup auf eine zweite Alternative auf einem Webserver erstellen. Windows Media Player versucht automatisch, ein Rollover zu verschiedenen Protokollen gemäß den Einstellungen der Windows Media-Eigenschaft vorzunehmen, bevor sie die Rollover-URLs in der Wiedergabeliste ausprobieren.

Legen Sie einen Server- und Protokollrollover fest, indem Sie mehrere **REF-Elemente** nacheinander innerhalb eines **ENTRY-Elements** platzieren. Jedes **REF-Element** gibt einen alternativen Speicherort oder ein protokoll für eine Mediendatei oder einen Stream an.

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

 

 




