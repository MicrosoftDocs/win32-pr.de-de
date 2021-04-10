---
title: Protokollieren von Streamdaten
description: Protokollieren von Streamdaten
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Windows Media Metadatei-Wiedergabelisten, Protokollieren von Streamdaten
- Wiedergabelisten, Protokollieren von Streamdaten
- Metadatei-Wiedergabelisten, Protokollieren von Streamdaten
- Windows Media Metadatei-Wiedergabelisten, Datenstrom Protokollierung
- Wiedergabelisten, Datenstrom Protokollierung
- Metadatei-Wiedergabelisten, Datenstrom Protokollierung
- Protokollieren von Streamdaten
- Datenstrom Protokollierung
- Windows Media Player, Protokollieren von Streamdaten
- Windows Media Player, Datenstrom Protokollierung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100814"
---
# <a name="logging-stream-data"></a>Protokollieren von Streamdaten

Protokollierte Informationen können abgerufen und verwendet werden, um das Viewer-Verhalten zu ermitteln, z. b. wie oft ein Stream angezeigt wird, oder ob ein bestimmter Benutzer einen Stream und die Dauer der Qualität angezeigt hat.

Protokollierungs Informationen werden automatisch an den Server gesendet, von dem aus die Wiedergabeliste stammt. Sie können Protokollierungs Informationen auch an zusätzliche Server senden, einschließlich Webservern, die ausschließlich für die Protokollierung verwendet werden. Verwenden Sie hierzu das **LogURL** -Element, und geben Sie eine gültige URL für das **href** -Attribut an. Sie können **LogURL** -Elemente als untergeordnete Elemente des Elements **ASX** und als untergeordnete Elemente einzelner **Einstiegs** Elemente einschließen. Wenn die Wiedergabeliste erstmalig geöffnet wird, werden Protokollierungs Informationen an den Ursprungsserver und an jede URL gesendet **, die unter den unter** geordneten **LogURL** -Elementen des-Elements angegeben ist. Wenn dann jeder Eintrag erreicht wird, werden für diesen Eintrag spezifische Protokollierungs Informationen an jede URL gesendet, die unter den untergeordneten **LogURL** -Daten des **Entry** -Elements angegeben ist.

Das Windows Media-Format-SDK unterstützt das **LogURL** -Element über die **iwmsreadernetworkconfig** -Schnittstelle und die folgenden Methoden:


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



Zusätzlich zu den Informationen, die automatisch protokolliert werden, kann eine Metadatei-Wiedergabeliste benutzerdefinierte Informationen mithilfe des **param** -Elements protokollieren. Wenn Sie das **param** -Element auf diese Weise verwenden möchten, legen Sie das **Name** -Attribut auf "Log:" gefolgt von einem Protokoll Feldnamen und einem optionalen XML-Namespace fest, der vom Feldnamen durch einen anderen Doppelpunkt (":") getrennt ist. Alles nach dem zweiten Doppelpunkt wird als Namespace behandelt, sodass der Feldname keinen Doppelpunkt enthalten sollte.

Das im **Name** -Attribut angegebene Protokollfeld wird auf den Wert des **value** -Attributs festgelegt. Wenn das Protokoll nicht bereits ein Feld mit dem angegebenen Namen enthält, wird es hinzugefügt.

**Beispiel Code**


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




