---
title: Behandeln von Uniform Resource Locators
description: Eine Uniform Resource Locator (URL) ist eine kompakte Darstellung der Standort-und Zugriffsmethode für eine Ressource, die sich im Internet befindet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08157738d99e78ff4d458a3bdd1b1e2e661ce538
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104551316"
---
# <a name="handling-uniform-resource-locators"></a>Behandeln von Uniform Resource Locators

Eine Uniform Resource Locator (URL) ist eine kompakte Darstellung der Standort-und Zugriffsmethode für eine Ressource, die sich im Internet befindet. Jede URL besteht aus einem Schema (http, HTTPS oder FTP) und einer Schema spezifischen Zeichenfolge. Diese Zeichenfolge kann auch eine Kombination aus Verzeichnispfad, Such Zeichenfolge oder Name der Ressource enthalten. Die WinInet-Funktionen bieten die Möglichkeit, URLs zu erstellen, zu kombinieren, aufzulösen und zu kanonisieren. Weitere Informationen zu URLs finden Sie unter [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) für URL (Uniform Resource Locators).

Die URL-Funktionen arbeiten aufgabenorientiert. Der Inhalt und das Format der URL, die an die Funktion übergeben wird, werden nicht überprüft. Die aufrufende Anwendung sollte die Verwendung dieser Funktionen nachverfolgen, um sicherzustellen, dass die Daten im vorgesehenen Format vorliegen. Beispielsweise würde die [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) -Funktion das Zeichen "%" in die Escapesequenz "%25" konvertieren, wenn keine Flags verwendet werden. Wenn [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) für die kanonisierte URL verwendet wird, wird die Escapesequenz "%25" in die Escapesequenz "%2525" konvertiert, was nicht ordnungsgemäß funktioniert.

-   [Was ist eine kanonisierte URL?](#what-is-a-canonicalized-url)
-   [Verwenden der WinInet-Funktionen zum Verarbeiten von URLs](#using-the-wininet-functions-to-handle-urls)
-   [Kanonisierende URLs](#what-is-a-canonicalized-url)
-   [Kombinieren von Basis-und relativen URLs](#combining-base-and-relative-urls)
-   [Knacken von URLs](#cracking-urls)
-   [Erstellen von URLs](#creating-urls)
-   [Direktes Aufrufen von URLs](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a>Was ist eine kanonisierte URL?

Das Format aller URLs muss der akzeptierten Syntax und Semantik entsprechen, damit Sie über das Internet auf Ressourcen zugreifen können. Kanonisierung ist der Prozess, bei dem eine URL formatiert wird, um diese akzeptierte Syntax und Semantik zu befolgen.

Zeichen, die codiert werden müssen, enthalten alle Zeichen, die kein entsprechendes Grafikzeichen im US-ASCII-codierten Zeichensatz aufweisen (hexadezimal 80-FF, die nicht im codierten US-ASCII-Zeichensatz verwendet werden, und hexadezimale 00-1f und 7F, die Steuerzeichen sind, Leerzeichen, "%" (zum Codieren anderer Zeichen verwendet) und unsichere Zeichen (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] und ').

## <a name="using-the-wininet-functions-to-handle-urls"></a>Verwenden der WinInet-Funktionen zum Verarbeiten von URLs

In der folgenden Tabelle werden die URL-Funktionen zusammengefasst.



| Funktion                                                   | BESCHREIBUNG                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [**Internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | Kanonisiert die URL.                             |
| [**Internetcombineurl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | Kombiniert Basis-und relative URLs.                   |
| [**Internetcrackurl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | Analysiert eine URL-Zeichenfolge in-Komponenten.               |
| [**Internetkreateurl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | Erstellt eine URL-Zeichenfolge aus-Komponenten.              |
| [**InternetOpenURL**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | Startet das Abrufen einer FTP-, http-oder HTTPS-Ressource. |



 

## <a name="canonicalizing-urls"></a>Kanonisierende URLs

Die kanonialisierung einer URL ist der Prozess, bei dem eine URL, die möglicherweise unsichere Zeichen (z. b. Leerzeichen, reservierte Zeichen usw.) enthält, in ein akzeptiertes Format konvertiert wird.

Die [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) -Funktion kann zum kanonisieren von URLs verwendet werden. Diese Funktion ist sehr aufgabenorientiert, sodass die Anwendung die Verwendung sorgfältig verfolgen sollte. [**Internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) überprüft nicht, ob die an Sie übergebenen URL bereits kanonisiert ist und ob die zurückgegebene URL gültig ist.

Die folgenden fünf Flags steuern, wie [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) eine bestimmte URL behandelt. Die Flags können in Kombination verwendet werden. Wenn keine Flags verwendet werden, codiert die Funktion die URL standardmäßig.



| Wert                     | Bedeutung                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ICU- \_ Browser \_ Modus        | Codieren oder Decodieren Sie keine Zeichen nach " \# " oder "?", und entfernen Sie nachfolgende Leerzeichen nicht nach "?". Wenn dieser Wert nicht angegeben wird, wird die gesamte URL codiert, und nachfolgende Leerzeichen werden entfernt. |
| ICU- \_ Decodierung               | Konvertieren Sie alle% XX-Sequenzen in Zeichen, einschließlich Escapesequenzen, bevor die URL analysiert wird.                                                                                                          |
| nur in ICU codierende \_ \_ Leerzeichen \_ | Nur Leerzeichen codieren.                                                                                                                                                                                     |
| ICU \_ nicht \_ Codieren           | Nicht unsichere Zeichen in Escapesequenzen konvertieren.                                                                                                                                                   |
| ICU \_ No \_ Meta             | Entfernen Sie keine Metasequenzen (z. b. "." und "..") aus der URL.                                                                                                                                       |



 

Das Flag für die ICU- \_ Decodierung sollte nur für kanonisierte URLs verwendet werden, da davon ausgegangen wird, dass es sich bei allen% XX-Sequenzen um Escapecodes handelt, die in die durch den Code aufgeführten Zeichen konvertiert werden. Wenn die URL das Symbol "%" enthält, das nicht Teil eines Escapecodes ist, behandelt die ICU- \_ Decodierung Sie weiterhin als eins. Dieses Merkmal kann dazu führen, dass [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) eine ungültige URL erstellt.

Um [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) zum Zurückgeben einer vollständig decodierten URL verwenden zu können, müssen die ICU \_ -decodierungsflags und die ICU-Kennung nicht codiert \_ \_ werden. Dieses Setup geht davon aus, dass die an [**internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) übergebenen URL zuvor kanonisiert wurde.

## <a name="combining-base-and-relative-urls"></a>Kombinieren von Basis-und relativen URLs

Ein relative URL ist eine kompakte Darstellung des Speicher Orts einer Ressource in Relation zu einer absoluten Basis-URL. Die Basis-URL muss dem Parser bekannt sein und umfasst in der Regel das Schema, den Netzwerk Speicherort und Teile des URL-Pfads. Eine Anwendung kann [**internetcombineurl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) aufgerufen werden, um die relative URL mit ihrer Basis-URL zu kombinieren. [**Internetcombineurl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) wird die resultierende URL auch kanonisiert.

## <a name="cracking-urls"></a>Knacken von URLs

Die Funktion [**internetknackurl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) trennt eine URL in Ihre Komponenten Teile und gibt die von der URL- [**\_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) Struktur, die an die Funktion übermittelt wird, aufgeführten Komponenten zurück.

Die Komponenten, die die [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) Struktur bilden, sind die Schema Nummer, der Hostname, die Portnummer, der Benutzername, das Kennwort, der URL-Pfad und zusätzliche Informationen (z. b. Suchparameter). Jede Komponente, außer dem Schema und den Portnummern, verfügt über einen Zeichen folgen Member, der die Informationen enthält, und einen Member, der die Länge des Zeichen folgen Elements enthält. Das Schema und die Portnummern verfügen nur über einen Member, der den entsprechenden Wert speichert. Beide werden bei allen erfolgreichen Aufrufen von [**internetcrackurl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)zurückgegeben.

Um den Wert einer bestimmten Komponente in der Struktur der [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) zu erhalten, muss der Member, der die Zeichen folgen Länge dieser Komponente speichert, auf einen Wert ungleich 0 (null) festgelegt werden. Der Zeichen folgen Member kann entweder die Adresse eines Puffers oder **null** sein.

Wenn das Zeigermember die Adresse eines Puffers enthält, muss das Zeichen folgen Längen Element die Größe dieses Puffers enthalten. [**Internetcrackurl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) gibt die Komponenten Informationen als Zeichenfolge im Puffer zurück und speichert die Länge der Zeichenfolge im Zeichen folgen Längen Element.

Wenn das Zeigermember **null** ist, kann das Zeichen folgen Längen Element auf einen Wert ungleich 0 (null) festgelegt werden. [**Internetcrackurl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) speichert die Adresse des ersten Zeichens der URL-Zeichenfolge, die die Komponenten Informationen enthält, und legt die Zeichen folgen Länge auf die Anzahl der Zeichen im verbleibenden Teil der URL-Zeichenfolge fest, die sich auf die Komponente bezieht.

Alle Zeiger Elemente, die auf **null** festgelegt sind, mit einem Element, das nicht NULL ist, zeigen auf den entsprechenden Startpunkt in der URL-Zeichenfolge Die im Längen Element gespeicherte Länge muss verwendet werden, um das Ende der Informationen der einzelnen Komponente zu bestimmen.

Damit die Struktur der [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) ordnungsgemäß initialisiert wird, muss der **dwstructsize** -Member auf die Größe der [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) Struktur in Bytes festgelegt werden.

Im folgenden Beispiel werden die Komponenten der URL im Bearbeitungsfeld, IDC \_ PreOpen1, zurückgegeben, und die Komponenten werden an das Listenfeld IDC \_ preopenlist zurückgegeben. Wenn Sie nur die Informationen für eine einzelne Komponente anzeigen möchten, kopiert diese Funktion das Zeichen direkt nach den Informationen der Komponente in der Zeichenfolge und ersetzt diese temporär durch **null**.


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a>Erstellen von URLs

Die [**internetkreateurl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) -Funktion verwendet die Informationen in der Struktur der [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , um eine Uniform Resource Locator zu erstellen.

Die Komponenten, aus denen die [**URL- \_ Komponenten**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) Struktur besteht, sind das Schema, der Hostname, die Portnummer, der Benutzername, das Kennwort, der URL-Pfad und zusätzliche Informationen (z. b. Suchparameter). Jede Komponente, außer der Portnummer, verfügt über einen Zeichen folgen Member, der die Informationen enthält, und einen Member, der die Länge des Zeichen folgen Elements enthält.

Für jede erforderliche Komponente sollte das Zeigermember die Adresse des Puffers enthalten, der die Informationen enthält. Das Längen Element muss auf 0 (null) festgelegt werden, wenn das Zeigermember die Adresse einer null-terminierten Zeichenfolge enthält. Das Längen Element muss auf die Länge der Zeichenfolge festgelegt werden, wenn das Zeigermember die Adresse einer Zeichenfolge enthält, die nicht mit 0 (null) beendet wird. Das Zeiger Element von Komponenten, die nicht erforderlich sind, muss **null** sein.

## <a name="accessing-urls-directly"></a>Direktes Aufrufen von URLs

Auf FTP-und http-Ressourcen im Internet kann direkt mithilfe der Funktionen [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) zugegriffen werden. [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) öffnet eine Verbindung mit der Ressource an der URL, die an die Funktion übermittelt wurde. Wenn diese Verbindung hergestellt wird, können zwei Schritte ausgeführt werden. Wenn es sich bei der Ressource um eine Datei handelt, kann Sie von " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) " heruntergeladen werden. Zweitens: Wenn es sich bei der Ressource um ein Verzeichnis handelt, kann [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) die Dateien im Verzeichnis auflisten (außer bei Verwendung von CERN-Proxys). Weitere Informationen zu " [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)" finden Sie unter [Lesen von Dateien](common-functions.md). Weitere Informationen zu [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)finden Sie untersuchen [der nächsten Datei](common-functions.md).

Für Anwendungen, die über einen CERN-Proxy ausgeführt werden müssen, kann [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) für den Zugriff auf FTP-Verzeichnisse und-Dateien verwendet werden. Die FTP-Anforderungen werden verpackt, damit Sie wie eine HTTP-Anforderung angezeigt werden, die der CERN-Proxy akzeptieren würde.

[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) verwendet das [**hinternethandle**](appendix-a-hinternet-handles.md) , das von der [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion erstellt wurde, und die URL der Ressource. Die URL muss das Schema (http:, FTP:, file: \[ für eine lokale Datei \] oder https: für ein \[ Hypertext-Protokoll sicher \] ) und einen Netzwerk Speicherort (z `www.microsoft.com` . b.) enthalten. Die URL kann auch einen Pfad enthalten (z. b./isapi/gomscom.ASP? Target =/Windows/Feature/) und Ressourcen Name (z. b. default.htm). Für http-oder HTTPS-Anforderungen können zusätzliche Header eingeschlossen werden.

[**Internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (nur http-oder HTTPS-URLs) können das Handle verwenden, das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) zum Herunterladen der Ressource erstellt wurde.

Im folgenden Diagramm wird veranschaulicht, welche Handles für die einzelnen Funktionen verwendet werden können.

![mit Functions zu verwendende Handles](images/ax-wnt02.png)

Das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) erstellte Stamm- [**HINTERNET**](appendix-a-hinternet-handles.md) Handle wird von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)verwendet. Das **hinternethandle** , das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) erstellt wurde, kann von [**internetquerydataavailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**internetfindnextfile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (hier nicht gezeigt) und [**internetsetfilepointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (nur http-oder HTTPS-URLs) verwendet werden.

Weitere Informationen finden Sie unter [**HINTERNET Handles**](appendix-a-hinternet-handles.md).

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 