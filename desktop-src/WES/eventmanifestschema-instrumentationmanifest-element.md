---
title: instrumentationmanifest-Element
description: Der Stamm Knoten des Manifests.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- instrumentiermanifest-Element EventLog
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c15092d7a7eafd625e9c2026965af053d38fe4b9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104219087"
---
# <a name="instrumentationmanifest-element"></a>instrumentationmanifest-Element

Der Stamm Knoten des Manifests.

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
| [**Ener**](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [**InstrumentationType**](eventmanifestschema-instrumentationtype-complextype.md) | In diesem Abschnitt werden ein oder mehrere Ereignis Anbieter und die Ereignisse definiert, die Sie protokollieren.<br/>                                                                                                                                                                                                                     |
| [**Lokalisierung**](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [**Localizationtype**](eventmanifestschema-localizationtype-complextype.md)       | In diesem Abschnitt werden die lokalisierten Meldungs Zeichenfolgen definiert, die Consumer zur Anzeige verwenden Dieser Abschnitt enthält z. b. die lokalisierte Meldungs Zeichenfolge für den Namen des Anbieters, die von Ihnen definierten Ereignisse und alle von Ihnen definierten Ereignis Attribute, z. b. Kanäle, Tasks und OpCodes.<br/> |
| [**benötigten**](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)               | In diesem Abschnitt werden Metadatentypen definiert, die andere Manifeste verwenden können. Ein Beispiel finden Sie in der Winmeta.xml-Datei, die im \\ Ordner include des Windows SDK enthalten ist.<br/>                                                                                                                                    |



## <a name="remarks"></a>Bemerkungen

Das **instrumentationmanifest** -Element muss die folgenden Namespaces enthalten:

<dl> xmlns = " https://schemas.microsoft.com/win/2004/08/events "  
xmlns: Win = " https://manifests.microsoft.com/win/2004/08/windows/events "  
xmlns: XS = " https://www.w3.org/2001/XMLSchema "  
</dl>

Ein Manifest muss einen Instrumentations Abschnitt und einen Lokalisierungs Abschnitt enthalten. Der Instrumentations Abschnitt und der Metadatenabschnitt schließen sich gegenseitig aus (Sie können nicht beide Elemente im selben Manifest definieren). Obwohl Sie ein Manifest erstellen können, das einen Metadatenabschnitt enthält, wird es vom Dienst nicht verwendet. die einzigen Metadaten, die der Dienst erkennt, sind die Metadaten, die in der Winmeta.xml-Datei gefunden werden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Gerüst eines vollständig definierten Instrumentierungs Manifests.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





