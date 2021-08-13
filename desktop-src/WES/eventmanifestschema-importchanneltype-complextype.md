---
title: Komplexer ImportChannelType-Typ
description: Identifiziert einen Kanal, der von einem anderen Anbieter oder in einem Manifest definiert wurde, das einen Metadatenabschnitt enthält.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- Komplexer ImportChannelType-Typ EventLog
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 66136ee767c16aa85bfcef33fd23d5d42817f844fc309f7633d2a3d2bd35f2e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471050"
---
# <a name="importchanneltype-complex-type"></a>Komplexer ImportChannelType-Typ

Identifiziert einen Kanal, der von einem anderen Anbieter oder in einem Manifest definiert wurde, das einen Metadatenabschnitt enthält.

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



| Name   | Type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Chid   | token                                                             | Ein Bezeichner, der den Kanal in der Liste der Kanäle, die der Anbieter definiert oder importiert, eindeutig identifiziert. Verwenden Sie diesen Wert, wenn Sie in einer Ereignisdefinition auf diesen Kanal verweisen. Wenn Sie keinen Kanalbezeichner angeben, verwenden Sie den Namen des Kanals, um in einer Ereignisdefinition auf diesen Kanal zu verweisen.<br/>  |
| name   | anyURI                                                            | Der Name des zu importierenden Kanals.<br/>                                                                                                                                                                                                                                                                          |
| Symbol | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf den Kanal in Ihrer Anwendung zu verweisen. Der [**Nachrichtencompiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das -Symbol, um eine Konstante für den Kanal in der Headerdatei zu erstellen, die der Compiler generiert. Wenn Sie kein Symbol angeben, generiert der Compiler ein Symbol für Sie.<br/> |



## <a name="remarks"></a>Hinweise

Das Manifest, das den importierten Kanal definiert hat, muss installiert werden, bevor Ihr Anbieter Ereignisse schreibt. Andernfalls können die Ereignisse nicht in den Kanal geschrieben werden (der Schreibvorgang ist erfolgreich, die Ereignisse werden einfach nicht in den Kanal geschrieben).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





