---
title: instrumentationManifest-Element
description: Der Stammknoten des Manifests.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- instrumentationManifest-Element EventLog
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7dac9ab8c8aa2a6caeacf43023c4995be69f293affd5dd5a904d7fb96d710266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343721"
---
# <a name="instrumentationmanifest-element"></a>instrumentationManifest-Element

Der Stammknoten des Manifests.

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                        | type                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Instrumentation**](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [**Instrumentationtype**](eventmanifestschema-instrumentationtype-complextype.md) | In diesem Abschnitt werden mindestens ein Ereignisanbieter und die ereignisse definiert, die protokolliert werden.<br/>                                                                                                                                                                                                                     |
| [**Lokalisierung**](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)       | In diesem Abschnitt werden die lokalisierten Meldungszeichenfolgen definiert, die Consumer für die Anzeige verwenden. Dieser Abschnitt würde beispielsweise die lokalisierte Nachrichtenzeichenfolge für den Namen Ihres Anbieters, die von Ihnen definierten Ereignisse und alle von Ihnen definierten Ereignisattribute wie Kanäle, Aufgaben und Opcodes enthalten.<br/> |
| [**Metadaten**](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)               | In diesem Abschnitt werden Metadatentypen definiert, die von anderen Manifesten verwendet werden können. Ein Beispiel finden Sie in der Winmeta.xml-Datei, die im Ordner Include des Windows SDK enthalten \\ ist.<br/>                                                                                                                                    |



## <a name="remarks"></a>Hinweise

Das **instrumentationManifest-Element** muss die folgenden Namespaces enthalten:

<dl> xmlns=" https://schemas.microsoft.com/win/2004/08/events "  
xmlns:win=" https://manifests.microsoft.com/win/2004/08/windows/events "  
xmlns:xs=" https://www.w3.org/2001/XMLSchema "  
</dl>

Ein Manifest muss einen Instrumentierungsabschnitt und einen Lokalisierungsabschnitt enthalten. Der Instrumentierungsabschnitt und der Metadatenabschnitt schließen sich gegenseitig aus (Sie können nicht beides im gleichen Manifest definieren). Obwohl Sie ein Manifest erstellen können, das einen Metadatenabschnitt enthält, wird es vom Dienst nicht verwendet. Die einzigen Metadaten, die der Dienst erkennt, sind die Metadaten, die in der datei Winmeta.xml gefunden werden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Gerüst eines vollständig definierten Instrumentierungsmanifests.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





