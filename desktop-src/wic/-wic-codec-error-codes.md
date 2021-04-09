---
description: Dieses Dokument enthält eine Liste der von Windows Imaging Component (WIC) definierten Fehlercodes.
ms.assetid: 1ded909c-311b-49e3-ba23-b22cd7a77bc6
title: Codec-Fehler Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd502ca1866114e2b471059bc9d9af1b0f96309f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958895"
---
# <a name="codec-error-codes"></a>Codec-Fehler Codes

Dieses Dokument enthält eine Liste der von Windows Imaging Component (WIC) definierten Fehlercodes.

-   [WIC-Fehler nach Code](#wic-errors-by-code)
-   [WIC-Fehler nach Wert](#wic-errors-by-value)

## <a name="wic-errors-by-code"></a>WIC-Fehler nach Code

In der folgenden Tabelle finden Sie eine Liste der Fehlercodes, die von den wicapis in alphabetischer Reihenfolge sortiert werden. 

| Fehlercode                                      | Fehlerwert                      |
|-------------------------------------------------|----------------------------------|
| wincodec \_ Err wurde \_ abgebrochen.                          | 0x80004004 (E \_ Abbrechen)            |
| wincodec \_ Err \_ AccessDenied                     | 0x80070005 (E \_ AccessDenied)     |
| wincodec \_ Err \_ alpassylock                    | 0x88982, f 0d                       |
| wincodec \_ Err- \_ badheader                        | 0x88982, f                       |
| wincodec \_ Err \_ badimage                         | 0x88982, f 60                       |
| wincodec \_ Err \_ BADMETADATAHEADER                | 0x88982, f 63                       |
| wincodec \_ Err \_ badstreamdata                    | 0x88982(f)                       |
| wincodec \_ Err \_ codecnominiatur                 | 0x88982, f                       |
| wincodec \_ Err- \_ codecpresent                     | 0x88982f 43                       |
| wincodec \_ Err \_ codectoomanyscanlines            | 0x88982f                       |
| wincodec \_ Err \_ componentinitializefailure       | 0x88982, s8b                       |
| wincodec \_ Err \_ componentnotfound                | 0x88982, f                       |
| wincodec \_ Err \_ DUPLICATEMETADATAPRESENT         | 0x88982, f-d                       |
| wincodec \_ Err- \_ frameout fehlt                     | 0x88982, f                       |
| allgemeiner wincodec \_ Err- \_ \_ Fehler                   | 0x80004005 (E \_ Fail)             |
| wincodec \_ Err \_ imagesizeoufür Frange              | 0x88982, f                       |
| wincodec \_ Err \_ insuffizientbuffer               | 0x88982, f 8 c                       |
| wincodec \_ Err \_ InternalError                    | 0x88982, f                       |
| wincodec \_ Err \_ invalidparameter                 | 0x80070057 (E \_ invalidArg)       |
| wincodec \_ Err \_ invalidquerycharacter            | 0x88982, f                       |
| wincodec \_ Err \_ invalidqueryrequest              | 0x88982, f                       |
| wincodec \_ Err \_ invalidregistration              | 0x88982f-a                       |
| wincodec \_ Err wurde benachrichtigt \_                   | 0x80004001 (E \_ notimpl)          |
| wincodec \_ Err \_ notinitialisiert                   | 0x88982"f"                       |
| wincodec \_ Err \_ outo-Memory                      | 0x8007000E (e \_ outo-Memory)      |
| wincodec \_ Err \_ palettenicht verfügbar               | 0x88982                       |
| wincodec \_ Err \_ propertynotfound                 | 0x88982f 40                       |
| wincodec \_ Err \_ propertynotsupported             | 0x88982, f                       |
| wincodec \_ Err \_ propertysize                     | 0x88982, f 42                       |
| wincodec \_ Err \_ propertyunexpectedtype           | 0x88982f                       |
| wincodec \_ Err \_ REQUESTONLYVALIDATMETADATAROOT   | 0x88982, f                       |
| wincodec \_ Err \_ sourcerectdoesnotmatchdimensions | 0x88982, f                       |
| wincodec \_ Err \_ streamwrite                      | 0x88982(f)                       |
| wincodec \_ Err \_ streamRead                       | 0x88982, nicht korrekt                       |
| wincodec \_ Err \_ streamnotavailable               | 0x88982, f 73                       |
| wincodec \_ Err-Dienst \_ Metadaten                  | 0x88982, f                       |
| wincodec \_ Err \_ unknownimageformat               | 0x88982, f                       |
| wincodec \_ Err \_ UNEXPECTEDMETADATATYPE           | 0x88982f 91                       |
| wincodec \_ Err \_ unexpectedsize                   | 0x88982f                       |
| wincodec \_ Err \_ unsupportedoperation             | 0x88982, f                       |
| wincodec \_ Err \_ unsupportedpixelformat           | 0x88982, f                       |
| wincodec \_ Err \_ unsupportedversion               | 0x88982, s0b                       |
| wincodec \_ Err \_ valueoutobt                  | 0x88982, f                       |
| wincodec \_ Err \_ valueoverflow                    | \_ \_ arithmetischer Überlauf in instiafe E \_ |
| wincodec \_ Err-Fehler \_ Status                       | 0x88982, f                       |



 

## <a name="wic-errors-by-value"></a>WIC-Fehler nach Wert

In der folgenden Tabelle finden Sie eine Liste der Fehlercodes, die von den wicapis in numerischer Reihenfolge sortiert werden. 

| Fehlercode                       | Fehlerwert                                     |
|----------------------------------|-------------------------------------------------|
| 0x80004005 (E \_ Fail)             | allgemeiner wincodec \_ Err- \_ \_ Fehler                   |
| 0x80070057 (E \_ invalidArg)       | wincodec \_ Err \_ invalidparameter                 |
| 0x8007000E (e \_ outo-Memory)      | wincodec \_ Err \_ outo-Memory                      |
| 0x80004001 (E \_ notimpl)          | wincodec \_ Err wurde benachrichtigt \_                   |
| 0x80004004 (E \_ Abbrechen)            | wincodec \_ Err wurde \_ abgebrochen.                          |
| 0x80070005 (E \_ AccessDenied)     | wincodec \_ Err \_ AccessDenied                     |
| \_ \_ arithmetischer Überlauf in instiafe E \_ | wincodec \_ Err \_ valueoverflow                    |
| 0x88982, f                       | wincodec \_ Err-Fehler \_ Status                       |
| 0x88982, f                       | wincodec \_ Err \_ valueoutobt                  |
| 0x88982, f                       | wincodec \_ Err \_ unknownimageformat               |
| 0x88982, s0b                       | wincodec \_ Err \_ unsupportedversion               |
| 0x88982"f"                       | wincodec \_ Err \_ notinitialisiert                   |
| 0x88982, f 0d                       | wincodec \_ Err \_ alpassylock                    |
| 0x88982f 40                       | wincodec \_ Err \_ propertynotfound                 |
| 0x88982, f                       | wincodec \_ Err \_ propertynotsupported             |
| 0x88982, f 42                       | wincodec \_ Err \_ propertysize                     |
| 0x88982f 43                       | wincodec \_ Err- \_ codecpresent                     |
| 0x88982, f                       | wincodec \_ Err \_ codecnominiatur                 |
| 0x88982                       | wincodec \_ Err \_ palettenicht verfügbar               |
| 0x88982f                       | wincodec \_ Err \_ codectoomanyscanlines            |
| 0x88982, f                       | wincodec \_ Err \_ InternalError                    |
| 0x88982, f                       | wincodec \_ Err \_ sourcerectdoesnotmatchdimensions |
| 0x88982, f                       | wincodec \_ Err \_ componentnotfound                |
| 0x88982, f                       | wincodec \_ Err \_ imagesizeoufür Frange              |
| 0x88982, f                       | wincodec \_ Err-Dienst \_ Metadaten                  |
| 0x88982, f 60                       | wincodec \_ Err \_ badimage                         |
| 0x88982, f                       | wincodec \_ Err- \_ badheader                        |
| 0x88982, f                       | wincodec \_ Err- \_ frameout fehlt                     |
| 0x88982, f 63                       | wincodec \_ Err \_ BADMETADATAHEADER                |
| 0x88982(f)                       | wincodec \_ Err \_ badstreamdata                    |
| 0x88982(f)                       | wincodec \_ Err \_ streamwrite                      |
| 0x88982, nicht korrekt                       | wincodec \_ Err \_ streamRead                       |
| 0x88982, f 73                       | wincodec \_ Err \_ streamnotavailable               |
| 0x88982, f                       | wincodec \_ Err \_ unsupportedpixelformat           |
| 0x88982, f                       | wincodec \_ Err \_ unsupportedoperation             |
| 0x88982f-a                       | wincodec \_ Err \_ invalidregistration              |
| 0x88982, s8b                       | wincodec \_ Err \_ componentinitializefailure       |
| 0x88982, f 8 c                       | wincodec \_ Err \_ insuffizientbuffer               |
| 0x88982, f-d                       | wincodec \_ Err \_ DUPLICATEMETADATAPRESENT         |
| 0x88982f                       | wincodec \_ Err \_ propertyunexpectedtype           |
| 0x88982f                       | wincodec \_ Err \_ unexpectedsize                   |
| 0x88982, f                       | wincodec \_ Err \_ invalidqueryrequest              |
| 0x88982f 91                       | wincodec \_ Err \_ UNEXPECTEDMETADATATYPE           |
| 0x88982, f                       | wincodec \_ Err \_ REQUESTONLYVALIDATMETADATAROOT   |
| 0x88982, f                       | wincodec \_ Err \_ invalidquerycharacter            |



 

 

 



