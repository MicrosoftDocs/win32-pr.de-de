---
title: usesgetlasterror-Attribut
description: Das Attribut \ "\"-GetLastError \ "signalisiert dem Aufrufer, dass GetLastError aufgerufen werden kann, um den Fehlercode abzurufen.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- attributgetlasterror-Attribut (Mittel l)
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725137"
---
# <a name="usesgetlasterror-attribute"></a>usesgetlasterror-Attribut

Das Attribut "$ **\[ GetLastError \]** " signalisiert dem Aufrufer, dass es [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen kann, um den Fehlercode abzurufen.

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Module-Attribute* 
</dt> <dd>

NULL oder mehr mittlere Attribute, die auf das [**Modul**](module.md)angewendet werden.

</dd> <dt>

*Modulname* 
</dt> <dd>

Der Bezeichnername des [**Moduls**](module.md).

</dd> <dt>

*Eintrags-ID* 
</dt> <dd>

Gibt den Einstiegspunkt des Moduls an – Funktionsname oder ganzzahlige Identifikationsnummer.

</dd> <dt>

*andere-Attribute* 
</dt> <dd>

NULL oder mehr mittlere Attribute, die auf die Remote Prozedur angewendet werden.

</dd> <dt>

*Rückgabetyp* 
</dt> <dd>

Der Typ der Daten, die von der Remote Prozedur bei Abschluss zurückgegeben werden.

</dd> <dt>

*function-name* 
</dt> <dd>

Der Name der Remote Prozedur, wie in der IDL-Datei definiert.

</dd> <dt>

*param-Liste* 
</dt> <dd>

NULL oder mehr Parameter für die Remote Prozedur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ usesgetlasterror \]** -Attribut kann für einen Modul Einstiegspunkt festgelegt werden, wenn der Einstiegspunkt die Windows-Funktion [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) zum Zurückgeben von Fehlercodes verwendet. Das-Attribut teilt dem Aufrufer mit, dass der Aufrufer dann [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen kann, um den Fehlercode abzurufen, wenn beim Aufrufen der Funktion ein Fehler auftritt.

## <a name="examples"></a>Beispiele

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 