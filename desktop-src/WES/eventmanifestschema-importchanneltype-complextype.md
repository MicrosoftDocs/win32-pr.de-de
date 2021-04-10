---
title: Komplexer importchanneltype-Typ
description: Identifiziert einen Kanal, der von einem anderen Anbieter oder einem Manifest definiert wurde, das einen Metadatenabschnitt enthält.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- Importchanneltype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7500d52179c3282c7f15dcdd5dd5a32620bbc076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103587"
---
# <a name="importchanneltype-complex-type"></a>Komplexer importchanneltype-Typ

Identifiziert einen Kanal, der von einem anderen Anbieter oder einem Manifest definiert wurde, das einen Metadatenabschnitt enthält.

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name   | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Chid   | token                                                             | Ein Bezeichner, der den Kanal in der Liste der vom Anbieter definierten oder importierten Kanäle eindeutig identifiziert. Verwenden Sie diesen Wert, wenn Sie in einer Ereignis Definition auf diesen Kanal verweisen. Wenn Sie keinen channelbezeichner angeben, verwenden Sie den Namen des Kanals, um auf diesen Kanal in einer Ereignis Definition zu verweisen.<br/>  |
| name   | anyURI                                                            | Der Name des zu importierenden Kanals.<br/>                                                                                                                                                                                                                                                                          |
| Symbol | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das für den Verweis auf den Kanal in Ihrer Anwendung verwendet werden soll. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Kanal in der vom Compiler generierten Header Datei zu erstellen. Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.<br/> |



## <a name="remarks"></a>Bemerkungen

Das Manifest, das den importierten Kanal definiert hat, muss installiert werden, bevor der Anbieter Ereignisse schreibt. Andernfalls können die Ereignisse nicht in den Kanal geschrieben werden (der Schreibvorgang ist erfolgreich, die Ereignisse werden einfach nicht in den Kanal geschrieben).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





