---
title: uuid-Attribut
description: Das \uuid\-Schnittstellenattribut legt einen UUID (Universally Unique Identifier) fest, der der Schnittstelle zugewiesen ist und ihn von anderen Schnittstellen unterscheidet.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- uuid-Attribut MIDL
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce85ad2014e1f0563e2c20af7abec3cc476fab330b38340162f28fd390a5f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066640"
---
# <a name="uuid-attribute"></a>uuid-Attribut

Das **\[ \] uuid-Schnittstellenattribut** kennzeichnet einen UUID (Universally Unique Identifier), der der Schnittstelle zugewiesen ist und ihn von anderen Schnittstellen unterscheidet.

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*string-uuid* 
</dt> <dd>

Gibt eine Zeichenfolge an, die aus acht Hexadezimalziffern gefolgt von einem Bindestrich und dann aus drei Gruppen von jeweils vier Hexadezimalziffern gefolgt von einem Bindestrich und dann 12 Hexadezimalziffern besteht. Sie können die UUID-Zeichenfolge in Anführungszeichen einschließen, außer wenn Sie den MIDL-Compilerschalter [**/osf**](-osf.md)verwenden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Laufzeitbibliothek verwendet die Schnittstellen-UUID, die das **\[ \] uuid-Attribut** festlegt, um die Kommunikation zwischen den Client- und Serveranwendungen herzustellen. Das **\[ \] uuid-Attribut** kann in der Schnittstellenattributliste für eine RPC-Schnittstelle oder eine COM-Schnittstelle angezeigt werden.

Für eine RPC-Schnittstelle muss die Schnittstellenattributliste entweder das **\[ \] uuid-Attribut** oder das **\[** [**lokale**](local.md) **\]** Attribut enthalten, und das von Ihnen verwendete Attribut muss genau einmal auftreten. Wenn die Liste das **\[ \] uuid-Attribut** enthält, kann sie auch das **\[** [](version.md) **\]** Versionsattribut enthalten.

Für eine COM-Schnittstelle (die durch das **\[** [](object.md) **\]** Objektschnittstellenattribut identifiziert wird) muss die Schnittstellenattributliste das **\[ \] uuid-Attribut** enthalten, kann jedoch nicht das **\[ \] Versionsattribut** enthalten. Die Liste für eine COM-Schnittstelle kann das **\[ lokale \]** Attribut enthalten, obwohl das **\[ uuid-Attribut \]** vorhanden ist.

Microsoft RPC unterstützt eine Erweiterung für DCE-IDL, mit der die UUID in doppelte Anführungszeichen ("" " ") eingeschlossen werden kann. Das Formular in Anführungszeichen wird für C-Compiler-Präprozessoren benötigt, die UUID-Zahlen als Gleitkommazahlen interpretieren.

Alle UUID-Werte sollten computergeneriert werden, um eindeutig zu sein. Verwenden Sie das Hilfsprogramm Uuidgen, um eindeutige UUID-Werte zu generieren.

Die UUID und die Versionsnummern der Schnittstelle werden verwendet, um zu bestimmen, ob der Client eine Bindung an den Server herstellen kann. Damit der Client an den Server gebunden werden kann, muss die in den Client- und Serverschnittstellen angegebene UUID identisch sein.

Beachten Sie, dass eine Schnittstelle ohne Attribute in eine IDL-Basisdatei importiert werden kann. Die Schnittstelle darf jedoch nur Datentypen ohne Prozeduren enthalten. Wenn selbst eine Prozedur in der Schnittstelle enthalten ist, muss ein lokales attribut oder ein UUID-Attribut angegeben werden.

## <a name="examples"></a>Beispiele

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[**lokal**](local.md)
</dt> <dt>

[**Objekt (object)**](object.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 




