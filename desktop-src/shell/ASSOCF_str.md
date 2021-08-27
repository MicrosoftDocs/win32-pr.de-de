---
description: Stellt Informationen für die IQueryAssociations-Schnittstellenmethoden bereit.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: ASSOCF-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6920ef874833471d88c4d42a074661337469b11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477936"
---
# <a name="assocf-enumeration"></a>ASSOCF-Enumeration

Stellt Informationen für die [**IQueryAssociations-Schnittstellenmethoden**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) bereit.

## <a name="syntax"></a>Syntax

<span codelanguage="ManagedCPlusPlus"></span>


| C++ | 
|-----|
| <pre><code>typedef enum  {   ASSOCF_NONE                  = 0x00000000,  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,  ASSOCF_INIT_BYEXENAME        = 0x00000002,  ASSOCF_OPEN_BYEXENAME        = 0x00000002,  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,  ASSOCF_NOUSERSETTINGS        = 0x00000010,  ASSOCF_NOTRUNCATE            = 0x00000020,  ASSOCF_VERIFY                = 0x00000040,  ASSOCF_REMAPRUNDLL           = 0x00000080,  ASSOCF_NOFIXUPS              = 0x00000100,  ASSOCF_IGNOREBASECLASS       = 0x00000200,  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,  ASSOCF_IS_PROTOCOL           = 0x00001000,  ASSOCF_INIT_FOR_FILE         = 0x00002000} ASSOCF;</code></pre> | 




## <a name="constants"></a>Konstanten

 <span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ NONE** 

Keine der folgenden Optionen ist festgelegt.

 <span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ INIT \_ NOREMAPCLSID** 

Weist [**IQueryAssociations-Schnittstellenmethoden**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) an, CLSID-Werte nicht ProgID-Werten zuzuordnen.

 <span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ INIT \_ BYEXENAME** 

Identifiziert den Wert des *pwszAssoc-Parameters* von [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) als ausführbaren Dateinamen. Wenn dieses Flag nicht festgelegt ist, wird der Stammschlüssel auf die ProgID festgelegt, die dem **.exe** Schlüssel zugeordnet ist, anstatt auf die ProgID der ausführbaren Datei.

 <span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ OPEN \_ BYEXENAME** 

Identisch mit **ASSOCF \_ INIT \_ BYEXENAME**.

 <span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ INIT \_ DEFAULTTOSTAR** 

Gibt an, dass versucht werden soll, den vergleichbaren Wert aus dem Unterschlüssel abzurufen, wenn eine [**IQueryAssociations-Methode**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) den angeforderten Wert unter dem Stammschlüssel nicht **\*** findet.

 <span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ INIT \_ DEFAULTTOFOLDER** 

Gibt an, dass eine [**IQueryAssociations-Methode**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) versuchen soll, den vergleichbaren Wert aus dem **Ordnerunterschlüssel** abzurufen, wenn sie den angeforderten Wert unter dem Stammschlüssel nicht findet.

 <span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS** 

Gibt an, dass nur **HKEY \_ CLASSES \_ ROOT** durchsucht und **HKEY \_ CURRENT \_ USER** ignoriert werden soll.

 <span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOTRUNCATE** 

Gibt an, dass die Rückgabezeichenfolge nicht abgeschnitten werden soll. Geben Sie stattdessen einen Fehlerwert und die erforderliche Größe für die vollständige Zeichenfolge zurück.

 <span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF \_ VERIFY** 

Weist [**IQueryAssociations-Methoden**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) an, die Genauigkeit der Daten zu überprüfen. Mit dieser Einstellung können **IQueryAssociations-Methoden** Daten zur Überprüfung von der Festplatte des Benutzers lesen. Sie können z. B. den Anzeigenamen in der Registrierung anhand des in der .exe-Datei gespeicherten Namens überprüfen. Das Festlegen dieses Flags verringert in der Regel die Effizienz der Methode.

 <span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF \_ REMAPRUNDLL** 

Weist [**IQueryAssociations-Methoden**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) an, Rundll.exe zu ignorieren und Informationen über das Ziel zurückzugeben. **IQueryAssociations-Methoden** geben in der Regel Informationen zum ersten .exe oder .dll in einer Befehlszeichenfolge zurück. Wenn ein Befehl Rundll.exe verwendet, weist das Festlegen dieses Flags die Methode an, Rundll.exe zu ignorieren und Informationen zum Ziel zurückzugeben.

 <span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF \_ NOFIXUPS** 

Weist [**IQueryAssociations-Methoden**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) an, Fehler in der Registrierung nicht zu beheben, z. B. den Anzeigenamen einer Funktion, die nicht mit dem in der datei .exe gefundenen übereinstimmt.

 <span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS** 

Gibt an, dass der BaseClass-Wert ignoriert werden soll.

 <span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ INIT \_ IGNOREUNKNOWN** 

**Eingeführt in Windows 7.** Gibt an, dass die ProgID "Unknown" ignoriert werden soll. stattdessen schlägt fehl.

 <span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF \_ INIT \_ FIXED \_ PROGID** 

**Eingeführt in Windows 8**. Gibt an, dass die angegebene ProgID mithilfe der Systemstandardeinstellungen und nicht mit den aktuellen Benutzerstandardeinstellungen zugeordnet werden soll.

 <span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ IS \_ PROTOCOL** 

**Eingeführt in Windows 8**. Gibt an, dass der Wert ein Protokoll ist und mit den aktuellen Benutzerstandardwerten zugeordnet werden soll.

 <span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ INIT \_ FOR \_ FILE** 

**Eingeführt in Windows 8.1**. Gibt an, dass die ProgID einer Dateierweiterungs-basierten Zuordnung entspricht. Verwenden Sie zusammen mit **ASSOCF \_ INIT \_ FIXED \_ PROGID**.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]               |
| Unterstützte Mindestversion (Server) | Windows 2000 Server \[nur Desktop-Apps\]                                 |
| Header                   |  Shlwapi.h  |



## <a name="see-also"></a>Weitere Informationen

 [**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) 

 

 

© 2017 Microsoft. Alle Rechte vorbehalten.
