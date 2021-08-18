---
title: Protokollieren von Streamdaten
description: Protokollieren von Streamdaten
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Windows Wiedergabelisten von Medienmetadateien, Protokollieren von Streamdaten
- Wiedergabelisten,Protokollieren von Streamdaten
- Metafile-Wiedergabelisten, Protokollieren von Streamdaten
- Windows Wiedergabelisten von Medienmetadateien, Streamdatenprotokollierung
- Wiedergabelisten,Streamdatenprotokollierung
- Metafile-Wiedergabelisten, Streamdatenprotokollierung
- Protokollieren von Streamdaten
- Streamdatenprotokollierung
- Windows Media Player,Protokollierung von Streamdaten
- Windows Media Player,Streamdatenprotokollierung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0a2ae6fe4b647e8a5c19fc6f30562973b3280f37cd3af3a1b9d9093771959de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118864"
---
# <a name="logging-stream-data"></a>Protokollieren von Streamdaten

Protokollierte Informationen können erfasst und verwendet werden, um das Viewerverhalten zu bestimmen, z. B. wie oft ein Stream angezeigt wird oder ob ein bestimmter Benutzer einen Stream und wie lange in welcher Qualität angezeigt wird.

Protokollierungsinformationen werden automatisch an den Server gesendet, von dem die Wiedergabeliste stammt. Sie können Protokollierungsinformationen auch an zusätzliche Server senden, einschließlich Webserver, die Sie ausschließlich für die Protokollierung verwenden. Verwenden Sie hierzu das **LOGURL-Element,** und geben Sie eine gültige URL für das **HREF-Attribut** an. Sie können **LOGURL-Elemente** als untere Elemente des **ASX-Elements** und als untere Elemente einzelner **ENTRY-Elemente** enthalten. Wenn die Wiedergabeliste zum ersten Mal geöffnet wird, werden Protokollierungsinformationen an den Ursprungsserver und an jede URL gesendet, die in **logurl** children des **ASX-Elements angegeben** ist. Wenn dann jeder Eintrag erreicht wird, werden spezifische Protokollierungsinformationen für diesen Eintrag an jede URL gesendet, die in den unter **LOGURL** -Elemente des ENTRY-Elements angegebenen unteren **Elemente angegeben** ist.

Das Windows Media Format SDK unterstützt das **LOGURL-Element** über die **IWMSReaderNetworkConfig-Schnittstelle** und die folgenden Methoden:


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



Zusätzlich zu den informationen, die automatisch protokolliert werden, kann eine Metadateiwiedergabeliste benutzerdefinierte Informationen mithilfe des **PARAM-Elements** protokollieren. Um das **PARAM-Element** auf diese Weise zu verwenden, legen Sie das **NAME-Attribut** auf "log:" fest, gefolgt von einem Protokollfeldnamen und einem optionalen XML-Namespace, der durch einen anderen Doppelpunkt (":") vom Feldnamen getrennt ist. Alles nach dem zweiten Doppelpunkt wird als Namespace behandelt, sodass der Feldname keinen Doppelpunkt enthalten sollte.

Das im NAME-Attribut **angegebene Protokollfeld** wird auf den Wert des **VALUE-Attributs** festgelegt. Wenn das Protokoll noch kein Feld mit dem angegebenen Namen enthält, wird es hinzugefügt.

**Beispielcode**


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

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




