---
title: uuid-Attribut
description: Das \ UUID \ Interface-Attribut kennzeichnet einen universellen eindeutigen Bezeichner (UUID), der der-Schnittstelle zugewiesen ist und von anderen Schnittstellen unterschieden wird.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- uuid-Attribut-Mittel l
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718534"
---
# <a name="uuid-attribute"></a>uuid-Attribut

Das **\[ UUID \]** Interface-Attribut kennzeichnet einen universellen eindeutigen Bezeichner (UUID), der der-Schnittstelle zugewiesen ist und von anderen Schnittstellen unterschieden wird.

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Zeichenfolge-UUID* 
</dt> <dd>

Gibt eine Zeichenfolge an, die aus 8 hexadezimalen Ziffern gefolgt von einem Bindestrich und dann drei Gruppen von vier hexadezimalen Ziffern gefolgt von einem Bindestrich und dann 12 hexadezimal Ziffern besteht. Sie können die UUID-Zeichenfolge in Anführungszeichen einschließen, es sei denn, Sie verwenden den Mittel l-Compilerschalter [**/OSF**](-osf.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Lauf Zeit Bibliothek verwendet die von dem **\[ UUID \]** -Attribut Festlegung-Schnittstellen-UUID, um die Kommunikation zwischen Client-und Server Anwendungen zu unterstützen. Das **\[ UUID \]** -Attribut kann in der Liste der Schnittstellen Attribute entweder für eine RPC-Schnittstelle oder eine COM-Schnittstelle angezeigt werden.

Für eine RPC-Schnittstelle muss die Liste der Schnittstellen Attribute entweder das **\[ \] UUID** -Attribut oder das **\[** [**lokale**](local.md) **\]** Attribut enthalten, und das von Ihnen gewählte muss genau einmal erfolgen. Wenn die Liste das **\[ UUID \]** -Attribut enthält, kann Sie auch das **\[** [**Versions**](version.md) **\]** Attribut enthalten.

Für eine COM-Schnittstelle (identifiziert durch das **\[** [**Objekt**](object.md) **\]** Schnittstellen Attribut) muss die Schnittstellen Attribut Liste das **\[ UUID \]** -Attribut enthalten, aber es kann nicht das **\[ Versions \]** Attribut enthalten. Die Liste für eine COM-Schnittstelle kann das **\[ lokale \]** Attribut enthalten, auch wenn das **\[ UUID \]** -Attribut vorhanden ist.

Microsoft RPC unterstützt eine Erweiterung der DCE-IDL, die es ermöglicht, dass die UUID in doppelte Anführungszeichen ("" "") eingeschlossen wird. Das Formular in Anführungszeichen wird für C-Compiler-Präprozessoren benötigt, die UUID-Nummern als Gleit Komma Zahlen interpretieren.

Alle UUID-Werte sollten Computer generiert werden, um Eindeutigkeit sicherzustellen. Verwenden Sie das Hilfsprogramm uuidgen, um eindeutige UUID-Werte zu generieren.

Die UUID und die Versionsnummern der-Schnittstelle werden verwendet, um zu bestimmen, ob der Client an den Server gebunden werden kann. Damit der Client an den Server gebunden wird, muss die in den Client-und Server Schnittstellen angegebene UUID identisch sein.

Beachten Sie, dass eine Schnittstelle ohne Attribute in eine Basis-IDL-Datei importiert werden kann. Allerdings darf die-Schnittstelle nur Datentypen ohne Prozeduren enthalten. Wenn auch eine Prozedur in der Schnittstelle enthalten ist, muss ein lokales Attribut oder ein uuid-Attribut angegeben werden.

## <a name="examples"></a>Beispiele

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**nah**](local.md)
</dt> <dt>

[**Objekt (object)**](object.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 




