---
description: Öffnet ein vorhandenes Verzeichnis Objekt.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: Ntopendirectoryobject-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357569"
---
# <a name="ntopendirectoryobject-function"></a>Ntopendirectoryobject-Funktion

\[Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Öffnet ein vorhandenes Verzeichnis Objekt.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Directoryhandle* \[ vorgenommen\]
</dt> <dd>

Ein Handle für das neu geöffnete Verzeichnis Objekt.

</dd> <dt>

*DesiredAccess* \[ in\]
</dt> <dd>

Eine [**Zugriffs \_ Maske**](../secauthz/access-mask.md) , die den angeforderten Zugriff auf das Verzeichnis Objekt angibt. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                                      | Bedeutung                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <dt>**Verzeichnis \_ Abfrage**</dt> <dt>0x0001</dt> </dl>                                            | Abfrage Zugriff auf das Verzeichnis Objekt.<br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <dt>**Verzeichnis \_**</dt>Durchlaufen <dt>0x0002</dt> </dl>                                   | Name-Lookup-Zugriff auf das Verzeichnis Objekt.<br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <dt>**Verzeichnis \_ \_Objekt**</dt> " <dt>0x0004</dt> " erstellen </dl>                   | Name: Erstellen des Zugriffs auf das Verzeichnis Objekt.<br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <dt>**Verzeichnis \_ \_Unterverzeichnis**</dt> " <dt>0x0008</dt> " erstellen </dl> | Unterverzeichnis-Erstellungs Zugriff auf das Verzeichnis Objekt.<br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <dt>**Verzeichnis \_ Alle \_ Zugriffs**</dt> <dt>Standard \_ Rechte \_ erforderlich \| 0xF</dt> </dl> | Alle vorangehenden Rechte und die **\_ \_ erforderlichen Standard Rechte**.<br/> |



 

</dd> <dt>

*Objectattributes* \[ in\]
</dt> <dd>

Die Attribute für das Verzeichnis Objekt. Um die **Objekt \_ Attribut** Struktur zu initialisieren, verwenden Sie das **initializeobjectattributes** -Makro. Weitere Informationen finden Sie in der Dokumentation für diese Elemente in der Dokumentation für das WDK.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt Status \_ Erfolg oder einen Fehlerstatus zurück. Folgende Statuscodes sind möglich:



| Rückgabecode                                                                                                       | Beschreibung                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_nicht genügend \_ Ressourcen.**</dt> </dl>    | Ein temporärer Puffer, der für diese Funktion erforderlich ist, konnte nicht zugeordnet werden.<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**\_ungültiger \_ Parameter.**</dt> </dl>         | Der angegebene objectattributes-Parameter war ein **null** -Zeiger, kein gültiger Zeiger auf eine **Objekt \_ Attribut** Struktur, oder einige der in der **Objekt \_ Attribut** Struktur angegebenen Member waren ungültig.<br/>                                                                          |
| <dl> <dt>**Status \_ Objekt \_ Name \_ ungültig**</dt> </dl>      | Der *objectattributes* -Parameter enthielt einen **objectName** -Member in der **Objekt \_ Attribut** Struktur, der ungültig war, da eine leere Zeichenfolge nach dem **\_ \_ Pfad \_ Trennzeichen für das Objektname** gefunden wurde.<br/>                                                                        |
| <dl> <dt>**der Status \_ Objekt \_ Name wurde \_ nicht \_ gefunden.**</dt> </dl>   | Der *objectattributes* -Parameter enthielt einen **objectName** -Member in der **Objekt \_ Attribut** Struktur, der nicht gefunden wurde.<br/>                                                                                                                                                           |
| <dl> <dt>**der Status \_ Objekt \_ Pfad wurde \_ nicht \_ gefunden.**</dt> </dl>   | Der *objectattributes* -Parameter enthielt einen **objectName** -Member in der **Objekt \_ Attribut** Struktur mit einem Objekt Pfad, der nicht gefunden wurde. <br/>                                                                                                                                      |
| <dl> <dt>**Status \_ Objekt \_ Pfad \_ Syntax \_ schlecht**</dt> </dl> | Der *objectattributes* -Parameter enthielt keinen **RootDirectory** -Member, aber das **objectName** -Element in der **Objekt \_ Attribut** Struktur war eine leere Zeichenfolge oder enthielt kein **\_ \_ Pfad \_ Trennzeichen für den Objektnamen** . Dies weist auf eine falsche Syntax für den Objekt Pfad hin.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ntquerydirectoryobject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
